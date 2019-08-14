---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861189"
---
## <a name="250---july-2019"></a><span data-ttu-id="42eb8-101">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="42eb8-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-102">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-103">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="42eb8-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="42eb8-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="42eb8-105">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="42eb8-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="42eb8-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-106">Az.Automation</span></span>
* <span data-ttu-id="42eb8-107">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="42eb8-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-109">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="42eb8-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-110">Az.Compute</span></span>
* <span data-ttu-id="42eb8-111">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="42eb8-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="42eb8-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42eb8-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="42eb8-113">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="42eb8-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="42eb8-114">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="42eb8-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-115">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-116">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="42eb8-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="42eb8-117">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="42eb8-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42eb8-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-118">Az.EventHub</span></span>
* <span data-ttu-id="42eb8-119">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="42eb8-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="42eb8-120">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="42eb8-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42eb8-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-121">Az.KeyVault</span></span>
* <span data-ttu-id="42eb8-122">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="42eb8-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42eb8-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-123">Az.LogicApp</span></span>
* <span data-ttu-id="42eb8-124">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="42eb8-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="42eb8-125">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="42eb8-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="42eb8-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-126">Az.ManagedServices</span></span>
* <span data-ttu-id="42eb8-127">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="42eb8-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-128">Az.Network</span></span>
* <span data-ttu-id="42eb8-129">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="42eb8-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="42eb8-130">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-130">New cmdlets</span></span>
        - <span data-ttu-id="42eb8-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42eb8-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42eb8-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42eb8-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42eb8-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42eb8-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42eb8-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42eb8-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="42eb8-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="42eb8-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="42eb8-139">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="42eb8-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="42eb8-140">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="42eb8-141">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag do wskazywania, czy stosowanie zasad sieciowych w prywatnym punkcie końcowym w tej podsieci ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="42eb8-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="42eb8-142">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag do wskazywania, czy stosowanie zasad sieciowych w prywatnej usłudze łączenia w tej podsieci ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="42eb8-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="42eb8-143">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="42eb8-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="42eb8-144">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="42eb8-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="42eb8-145">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-145">Updated cmdlets</span></span>
        - <span data-ttu-id="42eb8-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42eb8-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42eb8-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="42eb8-149">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="42eb8-150">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="42eb8-151">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="42eb8-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="42eb8-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="42eb8-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="42eb8-155">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="42eb8-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="42eb8-156">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="42eb8-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="42eb8-157">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="42eb8-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="42eb8-159">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="42eb8-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="42eb8-160">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="42eb8-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-162">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="42eb8-163">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="42eb8-164">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="42eb8-165">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="42eb8-166">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="42eb8-167">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="42eb8-168">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="42eb8-169">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="42eb8-170">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="42eb8-171">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="42eb8-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-172">Az.Resources</span></span>
- <span data-ttu-id="42eb8-173">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="42eb8-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="42eb8-174">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="42eb8-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42eb8-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42eb8-175">Az.ServiceBus</span></span>
* <span data-ttu-id="42eb8-176">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="42eb8-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="42eb8-177">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="42eb8-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-178">Az.Sql</span></span>
* <span data-ttu-id="42eb8-179">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="42eb8-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="42eb8-180">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="42eb8-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="42eb8-181">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="42eb8-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-182">Az.Storage</span></span>
* <span data-ttu-id="42eb8-183">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="42eb8-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="42eb8-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="42eb8-184">Az.StorageSync</span></span>
* <span data-ttu-id="42eb8-185">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="42eb8-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="42eb8-186">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="42eb8-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-187">Az.Websites</span></span>
* <span data-ttu-id="42eb8-188">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="42eb8-189">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="42eb8-190">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="42eb8-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="42eb8-191">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-192">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-193">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="42eb8-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="42eb8-194">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="42eb8-195">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="42eb8-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="42eb8-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="42eb8-196">Az.Advisor</span></span>
* <span data-ttu-id="42eb8-197">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="42eb8-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="42eb8-198">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="42eb8-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="42eb8-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-199">Az.ApiManagement</span></span>
* <span data-ttu-id="42eb8-200">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="42eb8-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="42eb8-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42eb8-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="42eb8-202">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="42eb8-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="42eb8-203">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="42eb8-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="42eb8-204">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="42eb8-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="42eb8-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42eb8-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="42eb8-206">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="42eb8-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-207">Az.Automation</span></span>
* <span data-ttu-id="42eb8-208">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-209">Az.Compute</span></span>
* <span data-ttu-id="42eb8-210">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-211">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-212">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="42eb8-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42eb8-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42eb8-213">Az.EventGrid</span></span>
* <span data-ttu-id="42eb8-214">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="42eb8-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42eb8-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-215">Az.IotHub</span></span>
* <span data-ttu-id="42eb8-216">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-217">Az.Network</span></span>
* <span data-ttu-id="42eb8-218">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="42eb8-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="42eb8-219">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="42eb8-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42eb8-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="42eb8-221">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="42eb8-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="42eb8-222">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="42eb8-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="42eb8-224">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="42eb8-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-226">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="42eb8-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-227">Az.Resources</span></span>
    - <span data-ttu-id="42eb8-228">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="42eb8-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="42eb8-229">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="42eb8-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="42eb8-230">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="42eb8-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="42eb8-231">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="42eb8-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42eb8-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42eb8-232">Az.ServiceBus</span></span>
* <span data-ttu-id="42eb8-233">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="42eb8-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-234">Az.Sql</span></span>
* <span data-ttu-id="42eb8-235">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="42eb8-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="42eb8-236">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42eb8-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="42eb8-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42eb8-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42eb8-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42eb8-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="42eb8-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="42eb8-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42eb8-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="42eb8-243">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="42eb8-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-244">Az.Storage</span></span>
* <span data-ttu-id="42eb8-245">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="42eb8-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42eb8-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="42eb8-247">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="42eb8-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="42eb8-248">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="42eb8-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="42eb8-249">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="42eb8-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="42eb8-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="42eb8-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="42eb8-252">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="42eb8-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="42eb8-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42eb8-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="42eb8-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42eb8-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="42eb8-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="42eb8-255">Az.StorageSync</span></span>
* <span data-ttu-id="42eb8-256">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="42eb8-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="42eb8-257">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-258">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-259">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="42eb8-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="42eb8-260">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="42eb8-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="42eb8-261">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="42eb8-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="42eb8-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="42eb8-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="42eb8-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="42eb8-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-264">Az.Compute</span></span>
* <span data-ttu-id="42eb8-265">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="42eb8-266">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="42eb8-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="42eb8-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="42eb8-267">Az.Dns</span></span>
* <span data-ttu-id="42eb8-268">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42eb8-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42eb8-269">Az.EventGrid</span></span>
* <span data-ttu-id="42eb8-270">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="42eb8-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="42eb8-271">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-271">New cmdlets:</span></span>
    - <span data-ttu-id="42eb8-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42eb8-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42eb8-273">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42eb8-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42eb8-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42eb8-275">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="42eb8-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42eb8-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42eb8-277">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42eb8-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="42eb8-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="42eb8-279">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42eb8-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="42eb8-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="42eb8-281">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="42eb8-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="42eb8-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="42eb8-283">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="42eb8-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="42eb8-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="42eb8-285">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="42eb8-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="42eb8-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="42eb8-287">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="42eb8-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="42eb8-288">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="42eb8-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="42eb8-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="42eb8-290">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="42eb8-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="42eb8-291">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="42eb8-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="42eb8-292">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="42eb8-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="42eb8-293">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="42eb8-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="42eb8-294">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="42eb8-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="42eb8-295">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="42eb8-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="42eb8-296">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="42eb8-297">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="42eb8-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="42eb8-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="42eb8-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="42eb8-299">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="42eb8-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="42eb8-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="42eb8-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="42eb8-301">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="42eb8-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="42eb8-302">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="42eb8-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42eb8-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42eb8-303">Az.FrontDoor</span></span>
* <span data-ttu-id="42eb8-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="42eb8-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="42eb8-305">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="42eb8-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="42eb8-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="42eb8-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="42eb8-307">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="42eb8-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-308">Az.Network</span></span>
* <span data-ttu-id="42eb8-309">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="42eb8-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="42eb8-310">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-310">New cmdlets</span></span>
        - <span data-ttu-id="42eb8-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="42eb8-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="42eb8-312">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42eb8-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="42eb8-313">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-313">New cmdlets</span></span> 
        - <span data-ttu-id="42eb8-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42eb8-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="42eb8-315">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="42eb8-316">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-316">New cmdlets</span></span> 
        - <span data-ttu-id="42eb8-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="42eb8-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42eb8-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42eb8-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42eb8-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="42eb8-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="42eb8-322">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42eb8-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="42eb8-323">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-323">New cmdlets</span></span>
        - <span data-ttu-id="42eb8-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42eb8-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42eb8-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42eb8-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42eb8-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42eb8-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42eb8-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="42eb8-328">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="42eb8-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="42eb8-329">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="42eb8-330">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="42eb8-331">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42eb8-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="42eb8-332">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42eb8-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="42eb8-333">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42eb8-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="42eb8-334">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="42eb8-335">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="42eb8-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="42eb8-336">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="42eb8-337">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="42eb8-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="42eb8-338">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="42eb8-339">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="42eb8-340">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="42eb8-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="42eb8-341">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="42eb8-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="42eb8-342">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="42eb8-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="42eb8-343">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="42eb8-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="42eb8-344">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="42eb8-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="42eb8-345">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="42eb8-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="42eb8-346">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="42eb8-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="42eb8-347">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="42eb8-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="42eb8-348">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="42eb8-349">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="42eb8-350">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="42eb8-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="42eb8-352">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="42eb8-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-353">Az.Resources</span></span>
* <span data-ttu-id="42eb8-354">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="42eb8-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="42eb8-355">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="42eb8-356">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="42eb8-357">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="42eb8-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42eb8-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="42eb8-359">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="42eb8-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-360">Az.Sql</span></span>
* <span data-ttu-id="42eb8-361">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="42eb8-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="42eb8-362">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="42eb8-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="42eb8-363">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="42eb8-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="42eb8-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42eb8-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42eb8-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42eb8-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42eb8-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42eb8-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42eb8-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="42eb8-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="42eb8-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="42eb8-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-369">Az.Storage</span></span>
* <span data-ttu-id="42eb8-370">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="42eb8-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="42eb8-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="42eb8-372">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="42eb8-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="42eb8-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-374">Az.Websites</span></span>
* <span data-ttu-id="42eb8-375">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="42eb8-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="42eb8-376">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="42eb8-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="42eb8-377">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="42eb8-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42eb8-378">Az.Cdn</span></span>
* <span data-ttu-id="42eb8-379">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="42eb8-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-380">Az.Compute</span></span>
* <span data-ttu-id="42eb8-381">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="42eb8-382">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="42eb8-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42eb8-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-383">Az.EventHub</span></span>
* <span data-ttu-id="42eb8-384">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="42eb8-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="42eb8-385">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42eb8-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-386">Az.Network</span></span>
* <span data-ttu-id="42eb8-387">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="42eb8-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="42eb8-388">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="42eb8-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42eb8-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="42eb8-390">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="42eb8-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-392">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="42eb8-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42eb8-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42eb8-393">Az.ServiceBus</span></span>
* <span data-ttu-id="42eb8-394">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42eb8-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42eb8-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="42eb8-396">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="42eb8-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="42eb8-397">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-398">Az.Sql</span></span>
* <span data-ttu-id="42eb8-399">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="42eb8-400">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="42eb8-401">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="42eb8-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="42eb8-402">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="42eb8-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-403">Az.Websites</span></span>
* <span data-ttu-id="42eb8-404">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="42eb8-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="42eb8-405">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="42eb8-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-406">Az.ApiManagement</span></span>
* <span data-ttu-id="42eb8-407">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="42eb8-408">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="42eb8-409">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="42eb8-410">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="42eb8-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="42eb8-411">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="42eb8-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="42eb8-412">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="42eb8-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="42eb8-413">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="42eb8-414">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="42eb8-415">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="42eb8-416">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="42eb8-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="42eb8-417">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="42eb8-418">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="42eb8-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="42eb8-419">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="42eb8-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="42eb8-420">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="42eb8-421">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="42eb8-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="42eb8-422">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="42eb8-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="42eb8-423">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="42eb8-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="42eb8-424">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="42eb8-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="42eb8-425">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42eb8-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="42eb8-426">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="42eb8-427">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="42eb8-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="42eb8-428">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="42eb8-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="42eb8-429">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="42eb8-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="42eb8-430">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="42eb8-431">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="42eb8-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="42eb8-432">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="42eb8-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="42eb8-433">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="42eb8-434">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="42eb8-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="42eb8-435">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="42eb8-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="42eb8-436">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="42eb8-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="42eb8-437">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="42eb8-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="42eb8-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="42eb8-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="42eb8-439">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="42eb8-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="42eb8-440">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42eb8-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="42eb8-441">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="42eb8-442">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="42eb8-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="42eb8-443">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="42eb8-444">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="42eb8-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="42eb8-445">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="42eb8-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="42eb8-446">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42eb8-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="42eb8-447">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="42eb8-448">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="42eb8-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="42eb8-449">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="42eb8-450">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="42eb8-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="42eb8-451">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42eb8-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="42eb8-452">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="42eb8-453">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="42eb8-454">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="42eb8-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="42eb8-455">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="42eb8-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="42eb8-456">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="42eb8-457">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="42eb8-458">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="42eb8-459">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="42eb8-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="42eb8-460">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="42eb8-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="42eb8-461">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="42eb8-462">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="42eb8-463">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42eb8-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="42eb8-464">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="42eb8-465">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="42eb8-466">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="42eb8-467">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42eb8-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="42eb8-468">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="42eb8-469">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="42eb8-470">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="42eb8-471">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="42eb8-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="42eb8-472">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="42eb8-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="42eb8-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="42eb8-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="42eb8-474">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="42eb8-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="42eb8-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="42eb8-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="42eb8-476">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="42eb8-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="42eb8-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="42eb8-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="42eb8-478">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="42eb8-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="42eb8-479">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="42eb8-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="42eb8-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="42eb8-481">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="42eb8-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="42eb8-482">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="42eb8-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="42eb8-483">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="42eb8-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-484">Az.Automation</span></span>
* <span data-ttu-id="42eb8-485">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="42eb8-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="42eb8-486">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="42eb8-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="42eb8-487">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="42eb8-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="42eb8-488">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="42eb8-489">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="42eb8-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="42eb8-490">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="42eb8-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="42eb8-491">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="42eb8-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-492">Az.Compute</span></span>
* <span data-ttu-id="42eb8-493">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="42eb8-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="42eb8-494">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="42eb8-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-496">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42eb8-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42eb8-497">Az.Monitor</span></span>
* <span data-ttu-id="42eb8-498">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="42eb8-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-499">Az.Network</span></span>
* <span data-ttu-id="42eb8-500">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="42eb8-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="42eb8-501">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="42eb8-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="42eb8-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="42eb8-503">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="42eb8-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-504">Az.Resources</span></span>
* <span data-ttu-id="42eb8-505">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="42eb8-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-506">Az.Sql</span></span>
* <span data-ttu-id="42eb8-507">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="42eb8-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="42eb8-508">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-509">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-510">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="42eb8-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-512">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="42eb8-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="42eb8-513">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="42eb8-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-514">Az.Compute</span></span>
* <span data-ttu-id="42eb8-515">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="42eb8-516">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="42eb8-517">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="42eb8-518">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="42eb8-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="42eb8-519">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="42eb8-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="42eb8-520">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="42eb8-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="42eb8-521">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="42eb8-521">Breaking changes</span></span>
    - <span data-ttu-id="42eb8-522">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="42eb8-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="42eb8-523">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="42eb8-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="42eb8-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="42eb8-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="42eb8-525">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="42eb8-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="42eb8-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="42eb8-526">Az.Dns</span></span>
* <span data-ttu-id="42eb8-527">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="42eb8-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="42eb8-528">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="42eb8-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="42eb8-529">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="42eb8-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42eb8-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42eb8-530">Az.FrontDoor</span></span>
* <span data-ttu-id="42eb8-531">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42eb8-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="42eb8-532">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="42eb8-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="42eb8-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42eb8-533">Az.HDInsight</span></span>
* <span data-ttu-id="42eb8-534">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="42eb8-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42eb8-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="42eb8-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42eb8-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="42eb8-537">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42eb8-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="42eb8-538">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="42eb8-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="42eb8-539">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="42eb8-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="42eb8-540">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="42eb8-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42eb8-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42eb8-541">Az.Monitor</span></span>
* <span data-ttu-id="42eb8-542">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="42eb8-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="42eb8-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="42eb8-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="42eb8-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="42eb8-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="42eb8-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="42eb8-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="42eb8-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="42eb8-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="42eb8-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="42eb8-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="42eb8-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="42eb8-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42eb8-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42eb8-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42eb8-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42eb8-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42eb8-554">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="42eb8-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="42eb8-555">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="42eb8-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-556">Az.Network</span></span>
* <span data-ttu-id="42eb8-557">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="42eb8-558">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-558">New cmdlets</span></span>
        - <span data-ttu-id="42eb8-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="42eb8-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="42eb8-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="42eb8-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="42eb8-563">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-563">Updated cmdlets</span></span>
        - <span data-ttu-id="42eb8-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="42eb8-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="42eb8-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="42eb8-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="42eb8-566">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="42eb8-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="42eb8-567">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="42eb8-568">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42eb8-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="42eb8-570">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="42eb8-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="42eb8-571">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="42eb8-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="42eb8-572">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-574">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="42eb8-575">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42eb8-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="42eb8-576">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42eb8-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="42eb8-577">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="42eb8-578">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="42eb8-579">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="42eb8-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="42eb8-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="42eb8-580">Az.Relay</span></span>
* <span data-ttu-id="42eb8-581">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="42eb8-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42eb8-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42eb8-582">Az.ServiceBus</span></span>
* <span data-ttu-id="42eb8-583">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="42eb8-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-584">Az.Storage</span></span>
* <span data-ttu-id="42eb8-585">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="42eb8-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="42eb8-586">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="42eb8-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="42eb8-587">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="42eb8-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="42eb8-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="42eb8-589">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="42eb8-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="42eb8-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="42eb8-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="42eb8-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-593">Az.Websites</span></span>
* <span data-ttu-id="42eb8-594">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="42eb8-595">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="42eb8-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="42eb8-596">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42eb8-597">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="42eb8-597">Highlights since the last major release</span></span>
* <span data-ttu-id="42eb8-598">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="42eb8-598">General availability of `Az` module</span></span>
* <span data-ttu-id="42eb8-599">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42eb8-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42eb8-600">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42eb8-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42eb8-601">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42eb8-602">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="42eb8-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42eb8-603">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42eb8-604">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42eb8-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-605">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-606">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="42eb8-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="42eb8-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42eb8-607">Az.Batch</span></span>
* <span data-ttu-id="42eb8-608">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42eb8-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42eb8-609">Az.Cdn</span></span>
* <span data-ttu-id="42eb8-610">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-612">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-613">Az.Compute</span></span>
* <span data-ttu-id="42eb8-614">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="42eb8-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="42eb8-615">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-616">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-617">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-618">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="42eb8-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-620">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42eb8-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42eb8-621">Az.EventGrid</span></span>
* <span data-ttu-id="42eb8-622">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="42eb8-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42eb8-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-623">Az.EventHub</span></span>
* <span data-ttu-id="42eb8-624">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="42eb8-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="42eb8-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42eb8-625">Az.HDInsight</span></span>
* <span data-ttu-id="42eb8-626">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42eb8-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-627">Az.IotHub</span></span>
* <span data-ttu-id="42eb8-628">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42eb8-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-629">Az.KeyVault</span></span>
* <span data-ttu-id="42eb8-630">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-631">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="42eb8-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42eb8-632">Az.MachineLearning</span></span>
* <span data-ttu-id="42eb8-633">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="42eb8-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="42eb8-634">Az.Media</span></span>
* <span data-ttu-id="42eb8-635">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42eb8-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42eb8-636">Az.Monitor</span></span>
  * <span data-ttu-id="42eb8-637">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="42eb8-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="42eb8-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="42eb8-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="42eb8-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="42eb8-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="42eb8-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42eb8-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="42eb8-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42eb8-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="42eb8-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42eb8-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="42eb8-643">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="42eb8-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-644">Az.Network</span></span>
* <span data-ttu-id="42eb8-645">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-646">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="42eb8-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="42eb8-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="42eb8-648">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="42eb8-650">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="42eb8-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="42eb8-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="42eb8-652">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-654">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-655">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="42eb8-656">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="42eb8-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="42eb8-657">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="42eb8-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42eb8-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42eb8-658">Az.RedisCache</span></span>
* <span data-ttu-id="42eb8-659">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-660">Az.Resources</span></span>
* <span data-ttu-id="42eb8-661">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-662">Az.Sql</span></span>
* <span data-ttu-id="42eb8-663">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="42eb8-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="42eb8-664">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-665">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="42eb8-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="42eb8-666">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="42eb8-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="42eb8-667">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="42eb8-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="42eb8-668">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="42eb8-669">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-670">Az.Websites</span></span>
* <span data-ttu-id="42eb8-671">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="42eb8-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="42eb8-672">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="42eb8-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42eb8-673">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="42eb8-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="42eb8-674">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="42eb8-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="42eb8-675">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42eb8-676">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="42eb8-676">Highlights since the last major release</span></span>
* <span data-ttu-id="42eb8-677">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="42eb8-677">General availability of `Az` module</span></span>
* <span data-ttu-id="42eb8-678">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42eb8-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42eb8-679">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42eb8-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42eb8-680">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42eb8-681">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="42eb8-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42eb8-682">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42eb8-683">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42eb8-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-684">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-685">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="42eb8-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42eb8-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="42eb8-687">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="42eb8-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="42eb8-688">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="42eb8-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-689">Az.Automation</span></span>
* <span data-ttu-id="42eb8-690">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="42eb8-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="42eb8-691">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="42eb8-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="42eb8-692">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-693">Az.Compute</span></span>
* <span data-ttu-id="42eb8-694">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="42eb8-695">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="42eb8-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="42eb8-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="42eb8-697">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="42eb8-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-698">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-699">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="42eb8-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="42eb8-700">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="42eb8-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-701">Az.Resources</span></span>
* <span data-ttu-id="42eb8-702">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="42eb8-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="42eb8-703">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="42eb8-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="42eb8-704">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="42eb8-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="42eb8-705">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42eb8-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="42eb8-706">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="42eb8-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="42eb8-707">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42eb8-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-708">Az.Sql</span></span>
* <span data-ttu-id="42eb8-709">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="42eb8-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-710">Az.Storage</span></span>
* <span data-ttu-id="42eb8-711">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="42eb8-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42eb8-712">New-AzStorageContext</span></span>
* <span data-ttu-id="42eb8-713">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="42eb8-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="42eb8-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42eb8-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42eb8-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42eb8-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42eb8-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="42eb8-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="42eb8-718">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="42eb8-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="42eb8-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42eb8-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42eb8-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42eb8-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42eb8-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42eb8-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="42eb8-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42eb8-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="42eb8-723">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="42eb8-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42eb8-724">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="42eb8-724">Highlights since the last major release</span></span>
* <span data-ttu-id="42eb8-725">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="42eb8-725">General availability of `Az` module</span></span>
* <span data-ttu-id="42eb8-726">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42eb8-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42eb8-727">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42eb8-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42eb8-728">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42eb8-729">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="42eb8-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42eb8-730">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42eb8-731">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-732">Az.Automation</span></span>
* <span data-ttu-id="42eb8-733">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="42eb8-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="42eb8-734">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="42eb8-734">Dynamic grouping</span></span>
    * <span data-ttu-id="42eb8-735">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="42eb8-735">Pre-Post script</span></span>
    * <span data-ttu-id="42eb8-736">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="42eb8-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-737">Az.Compute</span></span>
* <span data-ttu-id="42eb8-738">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="42eb8-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="42eb8-739">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="42eb8-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42eb8-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-740">Az.KeyVault</span></span>
* <span data-ttu-id="42eb8-741">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-742">Az.Network</span></span>
* <span data-ttu-id="42eb8-743">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="42eb8-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="42eb8-744">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="42eb8-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-746">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="42eb8-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="42eb8-747">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="42eb8-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-748">Az.Resources</span></span>
* <span data-ttu-id="42eb8-749">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="42eb8-750">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="42eb8-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-751">Az.Sql</span></span>
* <span data-ttu-id="42eb8-752">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="42eb8-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-753">Az.Storage</span></span>
* <span data-ttu-id="42eb8-754">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="42eb8-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="42eb8-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42eb8-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42eb8-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42eb8-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="42eb8-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="42eb8-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="42eb8-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="42eb8-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-761">Az.Websites</span></span>
* <span data-ttu-id="42eb8-762">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="42eb8-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="42eb8-763">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="42eb8-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-764">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-765">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="42eb8-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="42eb8-766">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-767">Az.Automation</span></span>
* <span data-ttu-id="42eb8-768">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="42eb8-769">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="42eb8-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="42eb8-770">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="42eb8-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42eb8-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42eb8-771">Az.Cdn</span></span>
* <span data-ttu-id="42eb8-772">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="42eb8-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-773">Az.Compute</span></span>
* <span data-ttu-id="42eb8-774">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="42eb8-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-775">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-776">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="42eb8-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42eb8-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-777">Az.LogicApp</span></span>
* <span data-ttu-id="42eb8-778">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="42eb8-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-779">Az.Network</span></span>
* <span data-ttu-id="42eb8-780">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="42eb8-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-782">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="42eb8-783">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="42eb8-783">SDK Update</span></span>
* <span data-ttu-id="42eb8-784">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="42eb8-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="42eb8-785">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="42eb8-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-786">Az.Resources</span></span>
* <span data-ttu-id="42eb8-787">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="42eb8-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="42eb8-788">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="42eb8-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="42eb8-789">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="42eb8-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="42eb8-790">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="42eb8-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="42eb8-791">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="42eb8-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="42eb8-792">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="42eb8-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-793">Az.Sql</span></span>
* <span data-ttu-id="42eb8-794">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="42eb8-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="42eb8-795">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="42eb8-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-796">Az.Storage</span></span>
* <span data-ttu-id="42eb8-797">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="42eb8-798">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="42eb8-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="42eb8-800">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-801">Az.Automation</span></span>
* <span data-ttu-id="42eb8-802">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="42eb8-803">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="42eb8-804">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-806">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-807">Az.Compute</span></span>
* <span data-ttu-id="42eb8-808">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="42eb8-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="42eb8-809">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="42eb8-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="42eb8-810">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="42eb8-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="42eb8-811">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="42eb8-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-813">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="42eb8-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42eb8-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-814">Az.EventHub</span></span>
* <span data-ttu-id="42eb8-815">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="42eb8-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="42eb8-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-816">Az.KeyVault</span></span>
* <span data-ttu-id="42eb8-817">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="42eb8-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42eb8-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-818">Az.LogicApp</span></span>
* <span data-ttu-id="42eb8-819">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="42eb8-820">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="42eb8-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="42eb8-821">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="42eb8-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42eb8-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42eb8-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42eb8-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42eb8-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42eb8-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42eb8-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42eb8-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="42eb8-826">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="42eb8-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="42eb8-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42eb8-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42eb8-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42eb8-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="42eb8-831">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="42eb8-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42eb8-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42eb8-832">Az.Monitor</span></span>
* <span data-ttu-id="42eb8-833">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="42eb8-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-834">Az.Network</span></span>
* <span data-ttu-id="42eb8-835">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="42eb8-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="42eb8-837">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="42eb8-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="42eb8-838">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="42eb8-839">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="42eb8-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="42eb8-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-840">Az.Resources</span></span>
* <span data-ttu-id="42eb8-841">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="42eb8-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42eb8-842">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="42eb8-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="42eb8-843">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="42eb8-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="42eb8-844">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="42eb8-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-845">Az.Sql</span></span>
* <span data-ttu-id="42eb8-846">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="42eb8-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="42eb8-847">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="42eb8-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-848">Az.Websites</span></span>
* <span data-ttu-id="42eb8-849">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="42eb8-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="42eb8-850">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-851">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-852">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42eb8-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42eb8-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-853">Az.AnalysisServices</span></span>
<span data-ttu-id="42eb8-854">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="42eb8-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-855">Az.Compute</span></span>
* <span data-ttu-id="42eb8-856">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="42eb8-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="42eb8-857">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="42eb8-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="42eb8-858">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="42eb8-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-859">Az.RecoveryServices</span></span>
<span data-ttu-id="42eb8-860">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="42eb8-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-861">Az.Resources</span></span>
* <span data-ttu-id="42eb8-862">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="42eb8-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="42eb8-863">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="42eb8-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42eb8-864">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="42eb8-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="42eb8-865">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="42eb8-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-866">Az.Sql</span></span>
* <span data-ttu-id="42eb8-867">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42eb8-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="42eb8-868">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="42eb8-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="42eb8-869">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="42eb8-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="42eb8-870">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-871">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-872">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="42eb8-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42eb8-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="42eb8-874">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="42eb8-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="42eb8-876">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="42eb8-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="42eb8-877">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-878">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-879">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="42eb8-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42eb8-880">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42eb8-881">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="42eb8-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="42eb8-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="42eb8-882">Az.Aks</span></span>
* <span data-ttu-id="42eb8-883">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42eb8-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-884">Az.Automation</span></span>
* <span data-ttu-id="42eb8-885">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="42eb8-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="42eb8-886">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42eb8-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42eb8-887">Az.Cdn</span></span>
* <span data-ttu-id="42eb8-888">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-889">Az.Compute</span></span>
* <span data-ttu-id="42eb8-890">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="42eb8-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="42eb8-891">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42eb8-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="42eb8-892">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="42eb8-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="42eb8-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42eb8-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="42eb8-894">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42eb8-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42eb8-895">Az.DataFactory</span></span>
* <span data-ttu-id="42eb8-896">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="42eb8-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-898">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="42eb8-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="42eb8-899">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="42eb8-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="42eb8-900">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42eb8-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-901">Az.IotHub</span></span>
* <span data-ttu-id="42eb8-902">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="42eb8-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42eb8-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-903">Az.KeyVault</span></span>
* <span data-ttu-id="42eb8-904">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-905">Az.Network</span></span>
* <span data-ttu-id="42eb8-906">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-907">Az.Resources</span></span>
* <span data-ttu-id="42eb8-908">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="42eb8-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="42eb8-909">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="42eb8-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="42eb8-910">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42eb8-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="42eb8-911">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="42eb8-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="42eb8-912">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="42eb8-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="42eb8-913">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42eb8-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="42eb8-914">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="42eb8-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42eb8-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="42eb8-916">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="42eb8-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="42eb8-917">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="42eb8-917">Fix some error messages.</span></span>
* <span data-ttu-id="42eb8-918">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="42eb8-919">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42eb8-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42eb8-920">Az.SignalR</span></span>
* <span data-ttu-id="42eb8-921">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-922">Az.Sql</span></span>
* <span data-ttu-id="42eb8-923">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42eb8-924">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="42eb8-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="42eb8-925">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="42eb8-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="42eb8-926">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="42eb8-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-927">Az.Storage</span></span>
* <span data-ttu-id="42eb8-928">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42eb8-929">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="42eb8-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="42eb8-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="42eb8-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="42eb8-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="42eb8-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="42eb8-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="42eb8-932">Az.TrafficManager</span></span>
* <span data-ttu-id="42eb8-933">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-934">Az.Websites</span></span>
* <span data-ttu-id="42eb8-935">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="42eb8-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42eb8-936">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="42eb8-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="42eb8-937">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="42eb8-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="42eb8-938">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42eb8-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-939">Az.Accounts</span></span>
* <span data-ttu-id="42eb8-940">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="42eb8-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-941">Az.Compute</span></span>
* <span data-ttu-id="42eb8-942">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="42eb8-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="42eb8-943">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="42eb8-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="42eb8-944">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-946">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="42eb8-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="42eb8-947">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="42eb8-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42eb8-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42eb8-948">Az.EventGrid</span></span>
* <span data-ttu-id="42eb8-949">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="42eb8-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="42eb8-950">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="42eb8-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="42eb8-951">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="42eb8-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42eb8-952">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="42eb8-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42eb8-953">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="42eb8-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42eb8-954">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="42eb8-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="42eb8-955">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="42eb8-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42eb8-956">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="42eb8-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42eb8-957">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="42eb8-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42eb8-958">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="42eb8-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="42eb8-959">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="42eb8-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="42eb8-960">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42eb8-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42eb8-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-961">Az.IotHub</span></span>
* <span data-ttu-id="42eb8-962">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="42eb8-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42eb8-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42eb8-963">Az.LogicApp</span></span>
* <span data-ttu-id="42eb8-964">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="42eb8-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-965">Az.Resources</span></span>
* <span data-ttu-id="42eb8-966">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="42eb8-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="42eb8-967">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="42eb8-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="42eb8-968">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42eb8-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42eb8-969">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="42eb8-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="42eb8-970">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="42eb8-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="42eb8-971">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="42eb8-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42eb8-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42eb8-972">Az.SignalR</span></span>
* <span data-ttu-id="42eb8-973">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-974">Az.Sql</span></span>
* <span data-ttu-id="42eb8-975">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="42eb8-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42eb8-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-976">Az.Storage</span></span>
* <span data-ttu-id="42eb8-977">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="42eb8-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="42eb8-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42eb8-978">New-AzStorageContext</span></span>
* <span data-ttu-id="42eb8-979">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="42eb8-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="42eb8-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="42eb8-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-981">Az.Websites</span></span>
* <span data-ttu-id="42eb8-982">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="42eb8-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="42eb8-983">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="42eb8-984">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="42eb8-985">Ogólne</span><span class="sxs-lookup"><span data-stu-id="42eb8-985">General</span></span>

- <span data-ttu-id="42eb8-986">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="42eb8-986">General Availability of Az Module</span></span>
- <span data-ttu-id="42eb8-987">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="42eb8-987">Online help for each module</span></span>
- <span data-ttu-id="42eb8-988">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="42eb8-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="42eb8-989">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="42eb8-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="42eb8-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-990">Az.Accounts</span></span>
- <span data-ttu-id="42eb8-991">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42eb8-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="42eb8-992">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="42eb8-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42eb8-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-993">Az.ApiManagement</span></span>
- <span data-ttu-id="42eb8-994">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="42eb8-994">Fixes for #7002</span></span>
- <span data-ttu-id="42eb8-995">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="42eb8-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42eb8-996">Az.Batch</span></span>
- <span data-ttu-id="42eb8-997">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="42eb8-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="42eb8-998">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="42eb8-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="42eb8-999">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="42eb8-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="42eb8-1000">Az.Billing</span></span>
- <span data-ttu-id="42eb8-1001">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="42eb8-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="42eb8-1003">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="42eb8-1004">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="42eb8-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42eb8-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="42eb8-1006">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="42eb8-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="42eb8-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="42eb8-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="42eb8-1008">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="42eb8-1010">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="42eb8-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42eb8-1011">Az.Monitor</span></span>
- <span data-ttu-id="42eb8-1012">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="42eb8-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42eb8-1013">Az.KeyVault</span></span>
- <span data-ttu-id="42eb8-1014">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="42eb8-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="42eb8-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42eb8-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="42eb8-1016">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="42eb8-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="42eb8-1017">Az.Media</span></span>
- <span data-ttu-id="42eb8-1018">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="42eb8-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42eb8-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-1019">Az.Network</span></span>
<span data-ttu-id="42eb8-1020">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="42eb8-1021">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="42eb8-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="42eb8-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="42eb8-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="42eb8-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="42eb8-1030">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="42eb8-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42eb8-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="42eb8-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42eb8-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42eb8-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42eb8-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="42eb8-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="42eb8-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="42eb8-1037">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="42eb8-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="42eb8-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42eb8-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42eb8-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42eb8-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42eb8-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42eb8-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="42eb8-1041">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42eb8-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="42eb8-1042">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="42eb8-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="42eb8-1044">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="42eb8-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1045">Az.Profile</span></span>
- <span data-ttu-id="42eb8-1046">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42eb8-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="42eb8-1048">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="42eb8-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1049">Az.Resources</span></span>
- <span data-ttu-id="42eb8-1050">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42eb8-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="42eb8-1052">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="42eb8-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="42eb8-1053">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="42eb8-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="42eb8-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="42eb8-1055">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="42eb8-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="42eb8-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-1056">Az.Sql</span></span>
- <span data-ttu-id="42eb8-1057">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="42eb8-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="42eb8-1058">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="42eb8-1059">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="42eb8-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-1060">Az.Storage</span></span>
- <span data-ttu-id="42eb8-1061">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42eb8-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-1062">Az.Websites</span></span>
- <span data-ttu-id="42eb8-1063">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="42eb8-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="42eb8-1064">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="42eb8-1065">Ogólne</span><span class="sxs-lookup"><span data-stu-id="42eb8-1065">General</span></span>

* <span data-ttu-id="42eb8-1066">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="42eb8-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="42eb8-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1067">Az.Compute</span></span>

* <span data-ttu-id="42eb8-1068">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="42eb8-1070">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="42eb8-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="42eb8-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42eb8-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="42eb8-1072">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="42eb8-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="42eb8-1073">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="42eb8-1074">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42eb8-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="42eb8-1076">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="42eb8-1077">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="42eb8-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1078">Az.Resources</span></span>

* <span data-ttu-id="42eb8-1079">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="42eb8-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="42eb8-1080">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="42eb8-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-1081">Az.Sql</span></span>

* <span data-ttu-id="42eb8-1082">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="42eb8-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="42eb8-1083">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="42eb8-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="42eb8-1084">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="42eb8-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-1085">Az.Storage</span></span>

* <span data-ttu-id="42eb8-1086">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="42eb8-1087">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="42eb8-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="42eb8-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42eb8-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42eb8-1089">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="42eb8-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="42eb8-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42eb8-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="42eb8-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42eb8-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42eb8-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-1092">Az.Websites</span></span>

* <span data-ttu-id="42eb8-1093">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="42eb8-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="42eb8-1094">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="42eb8-1095">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="42eb8-1096">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42eb8-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42eb8-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="42eb8-1098">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="42eb8-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="42eb8-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42eb8-1099">Az.Automation</span></span>
* <span data-ttu-id="42eb8-1100">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="42eb8-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="42eb8-1101">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="42eb8-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="42eb8-1102">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="42eb8-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="42eb8-1103">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="42eb8-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="42eb8-1104">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="42eb8-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="42eb8-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1105">Az.Compute</span></span>
* <span data-ttu-id="42eb8-1106">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="42eb8-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="42eb8-1107">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="42eb8-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42eb8-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="42eb8-1109">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="42eb8-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="42eb8-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="42eb8-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="42eb8-1111">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="42eb8-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42eb8-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-1112">Az.Network</span></span>
* <span data-ttu-id="42eb8-1113">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="42eb8-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="42eb8-1114">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="42eb8-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="42eb8-1115">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="42eb8-1116">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42eb8-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="42eb8-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="42eb8-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="42eb8-1118">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="42eb8-1119">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="42eb8-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="42eb8-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="42eb8-1121">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="42eb8-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="42eb8-1122">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="42eb8-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="42eb8-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="42eb8-1123">Az.Relay</span></span>
* <span data-ttu-id="42eb8-1124">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="42eb8-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1125">Az.Resources</span></span>
* <span data-ttu-id="42eb8-1126">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="42eb8-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="42eb8-1127">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="42eb8-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="42eb8-1128">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="42eb8-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42eb8-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="42eb8-1130">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="42eb8-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="42eb8-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-1131">Az.Sql</span></span>
* <span data-ttu-id="42eb8-1132">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="42eb8-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="42eb8-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42eb8-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42eb8-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42eb8-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42eb8-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42eb8-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42eb8-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42eb8-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42eb8-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42eb8-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42eb8-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42eb8-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42eb8-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="42eb8-1141">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="42eb8-1142">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="42eb8-1143">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="42eb8-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42eb8-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42eb8-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="42eb8-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="42eb8-1148">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="42eb8-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="42eb8-1149">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="42eb8-1150">Ogólne</span><span class="sxs-lookup"><span data-stu-id="42eb8-1150">General</span></span>
* <span data-ttu-id="42eb8-1151">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="42eb8-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1152">Az.Profile</span></span>
* <span data-ttu-id="42eb8-1153">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="42eb8-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="42eb8-1154">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="42eb8-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="42eb8-1155">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="42eb8-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="42eb8-1156">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="42eb8-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="42eb8-1157">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="42eb8-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="42eb8-1158">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="42eb8-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="42eb8-1159">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="42eb8-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-1161">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1162">Az.Compute</span></span>
* <span data-ttu-id="42eb8-1163">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="42eb8-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="42eb8-1164">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="42eb8-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="42eb8-1165">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-1167">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="42eb8-1168">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="42eb8-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="42eb8-1169">Az.Insights</span></span>
* <span data-ttu-id="42eb8-1170">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="42eb8-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="42eb8-1171">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="42eb8-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="42eb8-1172">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="42eb8-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="42eb8-1173">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="42eb8-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-1174">Az.Network</span></span>
* <span data-ttu-id="42eb8-1175">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42eb8-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="42eb8-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="42eb8-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="42eb8-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="42eb8-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="42eb8-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42eb8-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="42eb8-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="42eb8-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="42eb8-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="42eb8-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="42eb8-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42eb8-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42eb8-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42eb8-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="42eb8-1183">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="42eb8-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1184">Az.Resources</span></span>
* <span data-ttu-id="42eb8-1185">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="42eb8-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="42eb8-1186">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="42eb8-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42eb8-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42eb8-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="42eb8-1188">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42eb8-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42eb8-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="42eb8-1190">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="42eb8-1191">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="42eb8-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="42eb8-1192">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="42eb8-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="42eb8-1193">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="42eb8-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="42eb8-1194">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="42eb8-1195">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="42eb8-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1196">Az.Profile</span></span>
* <span data-ttu-id="42eb8-1197">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="42eb8-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="42eb8-1198">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="42eb8-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1199">Az.Compute</span></span>
* <span data-ttu-id="42eb8-1200">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="42eb8-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="42eb8-1201">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42eb8-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42eb8-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="42eb8-1203">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="42eb8-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="42eb8-1204">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="42eb8-1205">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42eb8-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42eb8-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-1208">Az.Network</span></span>
* <span data-ttu-id="42eb8-1209">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="42eb8-1210">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1211">Az.Resources</span></span>
* <span data-ttu-id="42eb8-1212">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="42eb8-1213">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="42eb8-1214">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="42eb8-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="42eb8-1215">Azure.Storage</span></span>
* <span data-ttu-id="42eb8-1216">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="42eb8-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="42eb8-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="42eb8-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="42eb8-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42eb8-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42eb8-1219">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="42eb8-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="42eb8-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="42eb8-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42eb8-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="42eb8-1222">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42eb8-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42eb8-1223">Az.Compute</span></span>
* <span data-ttu-id="42eb8-1224">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="42eb8-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="42eb8-1225">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="42eb8-1226">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="42eb8-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="42eb8-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="42eb8-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="42eb8-1228">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42eb8-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42eb8-1229">Az.Network</span></span>
* <span data-ttu-id="42eb8-1230">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="42eb8-1231">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="42eb8-1231">new cmdlets added</span></span>
    - <span data-ttu-id="42eb8-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="42eb8-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="42eb8-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="42eb8-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42eb8-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="42eb8-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="42eb8-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="42eb8-1238">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="42eb8-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="42eb8-1239">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="42eb8-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="42eb8-1240">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="42eb8-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42eb8-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42eb8-1241">Az.RedisCache</span></span>
* <span data-ttu-id="42eb8-1242">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="42eb8-1243">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="42eb8-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="42eb8-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42eb8-1244">Az.Resources</span></span>
* <span data-ttu-id="42eb8-1245">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42eb8-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42eb8-1246">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="42eb8-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="42eb8-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42eb8-1247">Az.Sql</span></span>
* <span data-ttu-id="42eb8-1248">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="42eb8-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42eb8-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42eb8-1249">Az.Websites</span></span>
* <span data-ttu-id="42eb8-1250">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="42eb8-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="42eb8-1251">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="42eb8-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="42eb8-1252">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="42eb8-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="42eb8-1253">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="42eb8-1253">Initial Release</span></span>