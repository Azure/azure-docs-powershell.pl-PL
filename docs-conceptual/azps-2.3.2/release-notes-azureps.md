---
ms.openlocfilehash: 8fe835b1973b7d48f56f5e0e51b27053910ce7ec
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2019
ms.locfileid: "67193009"
---
## <a name="232---june-2019"></a><span data-ttu-id="0e6b7-101">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-101">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-102">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-103">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-103">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0e6b7-104">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0e6b7-104">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0e6b7-105">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="0e6b7-105">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0e6b7-106">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0e6b7-106">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0e6b7-107">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0e6b7-107">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-108">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-108">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-109">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-109">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0e6b7-110">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-110">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0e6b7-111">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0e6b7-111">Az.Dns</span></span>
* <span data-ttu-id="0e6b7-112">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-112">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e6b7-113">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e6b7-113">Az.EventGrid</span></span>
* <span data-ttu-id="0e6b7-114">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-114">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0e6b7-115">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-115">New cmdlets:</span></span>
    - <span data-ttu-id="0e6b7-116">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e6b7-116">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e6b7-117">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-117">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e6b7-118">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e6b7-118">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e6b7-119">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-119">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0e6b7-120">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e6b7-120">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e6b7-121">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-121">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e6b7-122">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0e6b7-122">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0e6b7-123">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-123">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e6b7-124">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0e6b7-124">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0e6b7-125">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-125">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0e6b7-126">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-126">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0e6b7-127">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-127">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0e6b7-128">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0e6b7-128">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0e6b7-129">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-129">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0e6b7-130">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-130">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0e6b7-131">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-131">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0e6b7-132">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-132">Updated cmdlets:</span></span>
    - <span data-ttu-id="0e6b7-133">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-133">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0e6b7-134">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-134">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0e6b7-135">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-135">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0e6b7-136">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="0e6b7-136">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0e6b7-137">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-137">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0e6b7-138">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="0e6b7-138">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0e6b7-139">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-139">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0e6b7-140">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-140">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0e6b7-141">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="0e6b7-141">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0e6b7-142">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-142">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0e6b7-143">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-143">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0e6b7-144">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e6b7-144">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0e6b7-145">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-145">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0e6b7-146">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-146">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e6b7-147">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-147">Az.FrontDoor</span></span>
* <span data-ttu-id="0e6b7-148">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0e6b7-148">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0e6b7-149">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-149">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0e6b7-150">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e6b7-150">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0e6b7-151">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-151">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-152">Az.Network</span></span>
* <span data-ttu-id="0e6b7-153">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-153">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0e6b7-154">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-154">New cmdlets</span></span>
        - <span data-ttu-id="0e6b7-155">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0e6b7-155">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0e6b7-156">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0e6b7-156">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0e6b7-157">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-157">New cmdlets</span></span> 
        - <span data-ttu-id="0e6b7-158">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0e6b7-158">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0e6b7-159">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e6b7-159">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0e6b7-160">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-160">New cmdlets</span></span> 
        - <span data-ttu-id="0e6b7-161">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e6b7-161">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0e6b7-162">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e6b7-162">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0e6b7-163">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e6b7-163">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0e6b7-164">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-164">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0e6b7-165">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-165">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0e6b7-166">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e6b7-166">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0e6b7-167">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-167">New cmdlets</span></span>
        - <span data-ttu-id="0e6b7-168">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e6b7-168">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e6b7-169">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e6b7-169">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e6b7-170">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e6b7-170">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e6b7-171">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-171">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0e6b7-172">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-172">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0e6b7-173">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-173">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0e6b7-174">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-174">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0e6b7-175">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-175">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0e6b7-176">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-176">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0e6b7-177">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0e6b7-177">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0e6b7-178">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-178">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0e6b7-179">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-179">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0e6b7-180">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-180">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0e6b7-181">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="0e6b7-181">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0e6b7-182">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-182">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0e6b7-183">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-183">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0e6b7-184">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0e6b7-184">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0e6b7-185">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="0e6b7-185">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0e6b7-186">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-186">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0e6b7-187">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="0e6b7-187">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0e6b7-188">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-188">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0e6b7-189">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="0e6b7-189">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0e6b7-190">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0e6b7-190">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0e6b7-191">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-191">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0e6b7-192">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-192">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0e6b7-193">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-193">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0e6b7-194">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-194">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e6b7-195">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-195">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e6b7-196">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-196">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-197">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-198">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-198">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0e6b7-199">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-199">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0e6b7-200">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-200">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0e6b7-201">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-201">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-202">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-202">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e6b7-203">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="0e6b7-203">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-204">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-205">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-205">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0e6b7-206">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-206">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0e6b7-207">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="0e6b7-207">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0e6b7-208">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e6b7-208">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e6b7-209">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e6b7-209">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e6b7-210">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e6b7-210">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e6b7-211">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0e6b7-211">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0e6b7-212">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0e6b7-212">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-213">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-214">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-214">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0e6b7-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="0e6b7-216">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="0e6b7-216">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0e6b7-217">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-217">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-218">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-219">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="0e6b7-219">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0e6b7-220">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0e6b7-220">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0e6b7-221">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-221">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0e6b7-222">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e6b7-222">Az.Cdn</span></span>
* <span data-ttu-id="0e6b7-223">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-223">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-224">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-224">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-225">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-225">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0e6b7-226">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e6b7-226">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e6b7-227">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-227">Az.EventHub</span></span>
* <span data-ttu-id="0e6b7-228">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-228">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0e6b7-229">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6b7-229">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-230">Az.Network</span></span>
* <span data-ttu-id="0e6b7-231">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="0e6b7-231">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0e6b7-232">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="0e6b7-232">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e6b7-233">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-233">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e6b7-234">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0e6b7-234">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-236">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-236">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e6b7-237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e6b7-237">Az.ServiceBus</span></span>
* <span data-ttu-id="0e6b7-238">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6b7-238">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-239">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-239">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e6b7-240">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-240">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0e6b7-241">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-241">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-242">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-242">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-243">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-243">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0e6b7-244">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-244">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0e6b7-245">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-245">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0e6b7-246">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-246">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-247">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-247">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-248">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-248">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0e6b7-249">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-249">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0e6b7-250">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e6b7-250">Az.ApiManagement</span></span>
* <span data-ttu-id="0e6b7-251">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-251">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0e6b7-252">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-252">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0e6b7-253">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-253">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0e6b7-254">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="0e6b7-254">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0e6b7-255">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-255">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0e6b7-256">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="0e6b7-256">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0e6b7-257">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-257">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0e6b7-258">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-258">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0e6b7-259">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e6b7-259">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0e6b7-260">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="0e6b7-260">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0e6b7-261">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-261">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0e6b7-262">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-262">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0e6b7-263">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-263">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0e6b7-264">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-264">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0e6b7-265">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-265">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0e6b7-266">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-266">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0e6b7-267">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-267">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0e6b7-268">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="0e6b7-268">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0e6b7-269">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-269">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0e6b7-270">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-270">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0e6b7-271">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-271">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0e6b7-272">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-272">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0e6b7-273">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-273">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0e6b7-274">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e6b7-274">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0e6b7-275">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-275">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0e6b7-276">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-276">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0e6b7-277">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-277">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0e6b7-278">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-278">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0e6b7-279">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-279">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0e6b7-280">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-280">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0e6b7-281">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="0e6b7-281">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0e6b7-282">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0e6b7-282">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0e6b7-283">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-283">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0e6b7-284">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-284">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0e6b7-285">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-285">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0e6b7-286">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="0e6b7-286">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0e6b7-287">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-287">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0e6b7-288">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-288">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0e6b7-289">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-289">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0e6b7-290">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-290">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0e6b7-291">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-291">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0e6b7-292">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-292">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0e6b7-293">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-293">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0e6b7-294">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-294">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0e6b7-295">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-295">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0e6b7-296">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-296">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0e6b7-297">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-297">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0e6b7-298">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0e6b7-299">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-299">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0e6b7-300">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-300">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0e6b7-301">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-301">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0e6b7-302">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-302">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0e6b7-303">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-303">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0e6b7-304">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-304">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0e6b7-305">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-305">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0e6b7-306">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-306">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0e6b7-307">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-307">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0e6b7-308">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-308">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0e6b7-309">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-309">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0e6b7-310">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-310">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0e6b7-311">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0e6b7-311">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0e6b7-312">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0e6b7-313">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0e6b7-314">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0e6b7-315">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="0e6b7-315">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0e6b7-316">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-316">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0e6b7-317">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0e6b7-317">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0e6b7-318">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-318">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0e6b7-319">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0e6b7-319">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0e6b7-320">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-320">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0e6b7-321">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0e6b7-321">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0e6b7-322">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-322">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0e6b7-323">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-323">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0e6b7-324">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-324">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0e6b7-325">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-325">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0e6b7-326">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-326">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0e6b7-327">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-327">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-328">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-328">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-329">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-329">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0e6b7-330">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0e6b7-330">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0e6b7-331">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0e6b7-331">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0e6b7-332">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-332">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0e6b7-333">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0e6b7-333">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0e6b7-334">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-334">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0e6b7-335">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-335">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-336">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-336">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-337">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-337">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0e6b7-338">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-338">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-339">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-339">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-340">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-340">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e6b7-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-341">Az.Monitor</span></span>
* <span data-ttu-id="0e6b7-342">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-342">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-343">Az.Network</span></span>
* <span data-ttu-id="0e6b7-344">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-344">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0e6b7-345">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-345">Updated cmdlet:</span></span>
        - <span data-ttu-id="0e6b7-346">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e6b7-346">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0e6b7-347">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0e6b7-347">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-348">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-349">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-349">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-350">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-351">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="0e6b7-351">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0e6b7-352">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-352">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-353">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-353">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-354">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="0e6b7-354">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e6b7-355">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-355">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e6b7-356">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-356">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0e6b7-357">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-357">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-358">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-359">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-359">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0e6b7-360">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-360">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0e6b7-361">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-361">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0e6b7-362">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-362">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0e6b7-363">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-363">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0e6b7-364">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="0e6b7-364">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0e6b7-365">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="0e6b7-365">Breaking changes</span></span>
    - <span data-ttu-id="0e6b7-366">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-366">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0e6b7-367">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-367">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0e6b7-368">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0e6b7-368">Az.DeploymentManager</span></span>
* <span data-ttu-id="0e6b7-369">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="0e6b7-369">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0e6b7-370">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0e6b7-370">Az.Dns</span></span>
* <span data-ttu-id="0e6b7-371">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="0e6b7-371">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0e6b7-372">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-372">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0e6b7-373">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-373">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e6b7-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-374">Az.FrontDoor</span></span>
* <span data-ttu-id="0e6b7-375">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-375">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0e6b7-376">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-376">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0e6b7-377">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e6b7-377">Az.HDInsight</span></span>
* <span data-ttu-id="0e6b7-378">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-378">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0e6b7-379">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e6b7-379">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0e6b7-380">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e6b7-380">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0e6b7-381">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e6b7-381">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0e6b7-382">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-382">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0e6b7-383">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-383">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0e6b7-384">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-384">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e6b7-385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-385">Az.Monitor</span></span>
* <span data-ttu-id="0e6b7-386">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-386">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0e6b7-387">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0e6b7-387">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0e6b7-388">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-388">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0e6b7-389">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0e6b7-389">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0e6b7-390">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-390">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0e6b7-391">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0e6b7-391">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0e6b7-392">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0e6b7-392">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0e6b7-393">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-393">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e6b7-394">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-394">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e6b7-395">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-395">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e6b7-396">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-396">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e6b7-397">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-397">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e6b7-398">[Więcej](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="0e6b7-398">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0e6b7-399">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-399">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-400">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-400">Az.Network</span></span>
* <span data-ttu-id="0e6b7-401">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-401">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0e6b7-402">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-402">New cmdlets</span></span>
        - <span data-ttu-id="0e6b7-403">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-403">New-AzNatGateway</span></span>
        - <span data-ttu-id="0e6b7-404">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-404">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0e6b7-405">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-405">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0e6b7-406">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-406">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0e6b7-407">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-407">Updated cmdlets</span></span>
        - <span data-ttu-id="0e6b7-408">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0e6b7-408">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0e6b7-409">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0e6b7-409">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0e6b7-410">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-410">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0e6b7-411">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-411">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0e6b7-412">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-412">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e6b7-413">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-413">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e6b7-414">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-414">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0e6b7-415">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-415">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0e6b7-416">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-416">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-417">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-417">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-418">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-418">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0e6b7-419">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-419">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0e6b7-420">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-420">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0e6b7-421">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-421">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0e6b7-422">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-422">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0e6b7-423">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-423">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0e6b7-424">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0e6b7-424">Az.Relay</span></span>
* <span data-ttu-id="0e6b7-425">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-425">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e6b7-426">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e6b7-426">Az.ServiceBus</span></span>
* <span data-ttu-id="0e6b7-427">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="0e6b7-427">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-428">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-429">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-429">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0e6b7-430">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-430">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0e6b7-431">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-431">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0e6b7-432">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-432">New-AzStorageAccount</span></span>
* <span data-ttu-id="0e6b7-433">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-433">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0e6b7-434">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-434">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0e6b7-435">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-435">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0e6b7-436">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-436">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-437">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-437">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-438">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e6b7-438">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0e6b7-439">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="0e6b7-439">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0e6b7-440">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-440">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e6b7-441">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-441">Highlights since the last major release</span></span>
* <span data-ttu-id="0e6b7-442">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-442">General availability of `Az` module</span></span>
* <span data-ttu-id="0e6b7-443">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e6b7-443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e6b7-444">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e6b7-444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e6b7-445">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e6b7-446">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e6b7-447">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e6b7-448">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-449">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-449">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-450">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="0e6b7-450">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0e6b7-451">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e6b7-451">Az.Batch</span></span>
* <span data-ttu-id="0e6b7-452">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-452">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e6b7-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e6b7-453">Az.Cdn</span></span>
* <span data-ttu-id="0e6b7-454">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e6b7-455">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-455">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e6b7-456">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-457">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-457">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-458">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-458">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0e6b7-459">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-460">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-460">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e6b7-461">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e6b7-461">Az.DataFactory</span></span>
* <span data-ttu-id="0e6b7-462">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-462">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-463">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-463">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-464">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-464">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e6b7-465">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e6b7-465">Az.EventGrid</span></span>
* <span data-ttu-id="0e6b7-466">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-466">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e6b7-467">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-467">Az.EventHub</span></span>
* <span data-ttu-id="0e6b7-468">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="0e6b7-468">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0e6b7-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e6b7-469">Az.HDInsight</span></span>
* <span data-ttu-id="0e6b7-470">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-470">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e6b7-471">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-471">Az.IotHub</span></span>
* <span data-ttu-id="0e6b7-472">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-472">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e6b7-473">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-473">Az.KeyVault</span></span>
* <span data-ttu-id="0e6b7-474">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-475">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-475">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0e6b7-476">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0e6b7-476">Az.MachineLearning</span></span>
* <span data-ttu-id="0e6b7-477">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0e6b7-478">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0e6b7-478">Az.Media</span></span>
* <span data-ttu-id="0e6b7-479">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-479">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e6b7-480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-480">Az.Monitor</span></span>
  * <span data-ttu-id="0e6b7-481">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-481">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0e6b7-482">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0e6b7-482">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0e6b7-483">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0e6b7-483">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0e6b7-484">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-484">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0e6b7-485">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-485">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0e6b7-486">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-486">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0e6b7-487">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="0e6b7-487">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-488">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-488">Az.Network</span></span>
* <span data-ttu-id="0e6b7-489">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-489">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-490">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-490">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0e6b7-491">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0e6b7-491">Az.NotificationHubs</span></span>
* <span data-ttu-id="0e6b7-492">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e6b7-493">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-493">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e6b7-494">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-494">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0e6b7-495">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0e6b7-495">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0e6b7-496">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-497">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-497">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-498">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-499">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-499">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0e6b7-500">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0e6b7-500">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0e6b7-501">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="0e6b7-501">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e6b7-502">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e6b7-502">Az.RedisCache</span></span>
* <span data-ttu-id="0e6b7-503">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-503">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-504">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-505">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-505">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-506">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-507">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="0e6b7-507">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0e6b7-508">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-508">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-509">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-509">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0e6b7-510">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-510">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0e6b7-511">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-511">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0e6b7-512">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-512">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0e6b7-513">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-513">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-514">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-514">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-515">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-515">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0e6b7-516">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-516">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e6b7-517">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-517">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0e6b7-518">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-518">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0e6b7-519">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-519">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e6b7-520">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-520">Highlights since the last major release</span></span>
* <span data-ttu-id="0e6b7-521">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-521">General availability of `Az` module</span></span>
* <span data-ttu-id="0e6b7-522">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e6b7-522">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e6b7-523">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e6b7-523">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e6b7-524">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-524">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e6b7-525">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-525">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e6b7-526">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-526">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e6b7-527">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-527">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-528">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-528">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-529">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0e6b7-529">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e6b7-530">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-530">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e6b7-531">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-531">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0e6b7-532">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="0e6b7-532">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-533">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-533">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-534">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-534">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0e6b7-535">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-535">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0e6b7-536">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-536">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-537">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-538">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-538">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0e6b7-539">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-539">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0e6b7-540">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-540">Az.ContainerInstance</span></span>
* <span data-ttu-id="0e6b7-541">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="0e6b7-541">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e6b7-542">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e6b7-542">Az.DataFactory</span></span>
* <span data-ttu-id="0e6b7-543">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-543">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0e6b7-544">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-544">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-545">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-545">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-546">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-546">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0e6b7-547">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-547">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0e6b7-548">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="0e6b7-548">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0e6b7-549">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0e6b7-549">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0e6b7-550">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="0e6b7-550">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0e6b7-551">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0e6b7-551">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-552">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-552">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-553">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-553">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-554">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-554">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-555">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-555">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0e6b7-556">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e6b7-556">New-AzStorageContext</span></span>
* <span data-ttu-id="0e6b7-557">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-557">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0e6b7-558">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0e6b7-558">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0e6b7-559">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0e6b7-559">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0e6b7-560">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-560">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0e6b7-561">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-561">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0e6b7-562">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="0e6b7-562">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0e6b7-563">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e6b7-563">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0e6b7-564">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e6b7-564">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0e6b7-565">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e6b7-565">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0e6b7-566">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e6b7-566">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0e6b7-567">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="0e6b7-567">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e6b7-568">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-568">Highlights since the last major release</span></span>
* <span data-ttu-id="0e6b7-569">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-569">General availability of `Az` module</span></span>
* <span data-ttu-id="0e6b7-570">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e6b7-570">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e6b7-571">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e6b7-571">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e6b7-572">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-572">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e6b7-573">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-573">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e6b7-574">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-574">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e6b7-575">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-575">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-576">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-576">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-577">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-577">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0e6b7-578">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="0e6b7-578">Dynamic grouping</span></span>
    * <span data-ttu-id="0e6b7-579">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-579">Pre-Post script</span></span>
    * <span data-ttu-id="0e6b7-580">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-580">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-581">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-582">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0e6b7-582">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0e6b7-583">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-583">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e6b7-584">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-584">Az.KeyVault</span></span>
* <span data-ttu-id="0e6b7-585">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-585">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-586">Az.Network</span></span>
* <span data-ttu-id="0e6b7-587">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="0e6b7-587">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0e6b7-588">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="0e6b7-588">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-589">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-590">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="0e6b7-590">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0e6b7-591">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="0e6b7-591">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-592">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-593">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-593">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0e6b7-594">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="0e6b7-594">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-595">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-595">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-596">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-596">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-597">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-597">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-598">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-598">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0e6b7-599">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-599">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e6b7-600">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-600">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e6b7-601">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-601">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e6b7-602">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0e6b7-602">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0e6b7-603">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0e6b7-603">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0e6b7-604">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-604">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-605">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-605">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-606">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-606">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0e6b7-607">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="0e6b7-607">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-608">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-609">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="0e6b7-609">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0e6b7-610">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-610">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-611">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-611">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-612">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-612">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0e6b7-613">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-613">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0e6b7-614">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="0e6b7-614">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e6b7-615">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e6b7-615">Az.Cdn</span></span>
* <span data-ttu-id="0e6b7-616">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="0e6b7-616">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-617">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-617">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-618">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-618">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e6b7-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e6b7-619">Az.DataFactory</span></span>
* <span data-ttu-id="0e6b7-620">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-620">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e6b7-621">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e6b7-621">Az.LogicApp</span></span>
* <span data-ttu-id="0e6b7-622">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="0e6b7-622">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-623">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-623">Az.Network</span></span>
* <span data-ttu-id="0e6b7-624">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="0e6b7-624">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-625">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-626">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-626">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0e6b7-627">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="0e6b7-627">SDK Update</span></span>
* <span data-ttu-id="0e6b7-628">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e6b7-628">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0e6b7-629">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e6b7-629">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-630">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-631">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-631">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0e6b7-632">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0e6b7-632">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0e6b7-633">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-633">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0e6b7-634">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0e6b7-634">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0e6b7-635">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-635">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0e6b7-636">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0e6b7-636">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-637">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-638">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-638">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0e6b7-639">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-639">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-640">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-641">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-641">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0e6b7-642">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-642">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0e6b7-643">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-643">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e6b7-644">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-644">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-645">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-645">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-646">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-646">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0e6b7-647">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-647">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0e6b7-648">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-648">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e6b7-649">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-649">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e6b7-650">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-650">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-651">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-651">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-652">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-652">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0e6b7-653">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="0e6b7-653">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0e6b7-654">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-654">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0e6b7-655">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-655">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-656">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-656">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-657">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="0e6b7-657">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e6b7-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-658">Az.EventHub</span></span>
* <span data-ttu-id="0e6b7-659">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-659">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0e6b7-660">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-660">Az.KeyVault</span></span>
* <span data-ttu-id="0e6b7-661">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e6b7-661">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e6b7-662">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e6b7-662">Az.LogicApp</span></span>
* <span data-ttu-id="0e6b7-663">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-663">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0e6b7-664">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="0e6b7-664">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0e6b7-665">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-665">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0e6b7-666">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e6b7-666">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e6b7-667">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e6b7-667">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e6b7-668">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e6b7-668">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e6b7-669">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e6b7-669">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0e6b7-670">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-670">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0e6b7-671">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-671">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e6b7-672">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-672">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e6b7-673">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-673">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e6b7-674">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-674">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0e6b7-675">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0e6b7-675">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e6b7-676">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-676">Az.Monitor</span></span>
* <span data-ttu-id="0e6b7-677">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-677">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-678">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-678">Az.Network</span></span>
* <span data-ttu-id="0e6b7-679">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0e6b7-679">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e6b7-680">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-680">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e6b7-681">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-681">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0e6b7-682">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-682">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0e6b7-683">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-683">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0e6b7-684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-684">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-685">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0e6b7-685">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0e6b7-686">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0e6b7-686">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0e6b7-687">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0e6b7-687">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0e6b7-688">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0e6b7-688">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-689">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-689">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-690">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0e6b7-690">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0e6b7-691">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-691">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-692">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-693">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0e6b7-693">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0e6b7-694">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-694">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-695">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-696">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0e6b7-696">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e6b7-697">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-697">Az.AnalysisServices</span></span>
<span data-ttu-id="0e6b7-698">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-698">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-699">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-700">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="0e6b7-700">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0e6b7-701">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e6b7-701">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0e6b7-702">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-702">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-703">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-703">Az.RecoveryServices</span></span>
<span data-ttu-id="0e6b7-704">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-704">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-705">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-705">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-706">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-706">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0e6b7-707">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0e6b7-707">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0e6b7-708">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="0e6b7-708">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0e6b7-709">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0e6b7-709">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-710">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-711">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-711">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0e6b7-712">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="0e6b7-712">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0e6b7-713">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="0e6b7-713">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0e6b7-714">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-714">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-715">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-715">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-716">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-716">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e6b7-717">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-717">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e6b7-718">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-718">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-719">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-719">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e6b7-720">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="0e6b7-720">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0e6b7-721">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-721">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-722">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-722">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-723">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e6b7-723">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e6b7-724">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-724">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e6b7-725">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0e6b7-725">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0e6b7-726">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0e6b7-726">Az.Aks</span></span>
* <span data-ttu-id="0e6b7-727">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-727">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e6b7-728">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-728">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-729">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-729">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0e6b7-730">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-730">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e6b7-731">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e6b7-731">Az.Cdn</span></span>
* <span data-ttu-id="0e6b7-732">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-732">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-733">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-733">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-734">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-734">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0e6b7-735">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e6b7-735">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0e6b7-736">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e6b7-736">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0e6b7-737">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e6b7-737">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0e6b7-738">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-738">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e6b7-739">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e6b7-739">Az.DataFactory</span></span>
* <span data-ttu-id="0e6b7-740">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="0e6b7-740">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-741">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-741">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-742">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="0e6b7-742">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0e6b7-743">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0e6b7-743">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0e6b7-744">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-744">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e6b7-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-745">Az.IotHub</span></span>
* <span data-ttu-id="0e6b7-746">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-746">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e6b7-747">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-747">Az.KeyVault</span></span>
* <span data-ttu-id="0e6b7-748">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-748">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-749">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-749">Az.Network</span></span>
* <span data-ttu-id="0e6b7-750">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-750">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-751">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-752">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0e6b7-752">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0e6b7-753">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-753">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0e6b7-754">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0e6b7-754">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0e6b7-755">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0e6b7-755">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0e6b7-756">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0e6b7-756">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0e6b7-757">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e6b7-757">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0e6b7-758">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0e6b7-758">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-759">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-759">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e6b7-760">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0e6b7-760">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0e6b7-761">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-761">Fix some error messages.</span></span>
* <span data-ttu-id="0e6b7-762">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-762">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0e6b7-763">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-763">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0e6b7-764">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0e6b7-764">Az.SignalR</span></span>
* <span data-ttu-id="0e6b7-765">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-765">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-766">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-767">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-767">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e6b7-768">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="0e6b7-768">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0e6b7-769">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="0e6b7-769">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0e6b7-770">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="0e6b7-770">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-771">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-772">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-772">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e6b7-773">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-773">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0e6b7-774">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0e6b7-774">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0e6b7-775">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0e6b7-775">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0e6b7-776">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0e6b7-776">Az.TrafficManager</span></span>
* <span data-ttu-id="0e6b7-777">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-777">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-778">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-778">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-779">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="0e6b7-779">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e6b7-780">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-780">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0e6b7-781">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="0e6b7-781">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0e6b7-782">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-782">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e6b7-783">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-783">Az.Accounts</span></span>
* <span data-ttu-id="0e6b7-784">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0e6b7-784">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-785">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-786">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-786">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0e6b7-787">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-787">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0e6b7-788">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-788">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-789">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-789">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-790">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-790">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0e6b7-791">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="0e6b7-791">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e6b7-792">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e6b7-792">Az.EventGrid</span></span>
* <span data-ttu-id="0e6b7-793">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-793">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0e6b7-794">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0e6b7-794">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0e6b7-795">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-795">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0e6b7-796">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="0e6b7-796">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0e6b7-797">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="0e6b7-797">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0e6b7-798">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-798">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0e6b7-799">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-799">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0e6b7-800">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="0e6b7-800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0e6b7-801">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="0e6b7-801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0e6b7-802">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-802">Dead letter endpoint.</span></span>
* <span data-ttu-id="0e6b7-803">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-803">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0e6b7-804">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-804">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e6b7-805">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-805">Az.IotHub</span></span>
* <span data-ttu-id="0e6b7-806">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="0e6b7-806">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e6b7-807">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e6b7-807">Az.LogicApp</span></span>
* <span data-ttu-id="0e6b7-808">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-808">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-809">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-809">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-810">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-810">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0e6b7-811">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0e6b7-811">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0e6b7-812">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0e6b7-812">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0e6b7-813">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0e6b7-813">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0e6b7-814">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-814">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0e6b7-815">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0e6b7-815">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0e6b7-816">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0e6b7-816">Az.SignalR</span></span>
* <span data-ttu-id="0e6b7-817">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-817">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-818">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-818">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-819">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-819">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e6b7-820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-820">Az.Storage</span></span>
* <span data-ttu-id="0e6b7-821">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="0e6b7-821">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0e6b7-822">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e6b7-822">New-AzStorageContext</span></span>
* <span data-ttu-id="0e6b7-823">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="0e6b7-823">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0e6b7-824">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0e6b7-824">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-825">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-825">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-826">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-826">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0e6b7-827">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-827">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0e6b7-828">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-828">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0e6b7-829">Ogólne</span><span class="sxs-lookup"><span data-stu-id="0e6b7-829">General</span></span>

- <span data-ttu-id="0e6b7-830">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="0e6b7-830">General Availability of Az Module</span></span>
- <span data-ttu-id="0e6b7-831">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-831">Online help for each module</span></span>
- <span data-ttu-id="0e6b7-832">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-832">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0e6b7-833">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="0e6b7-833">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0e6b7-834">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-834">Az.Accounts</span></span>
- <span data-ttu-id="0e6b7-835">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-835">Changed from Az.Profile</span></span>
- <span data-ttu-id="0e6b7-836">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-836">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0e6b7-837">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e6b7-837">Az.ApiManagement</span></span>
- <span data-ttu-id="0e6b7-838">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="0e6b7-838">Fixes for #7002</span></span>
- <span data-ttu-id="0e6b7-839">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-839">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0e6b7-840">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e6b7-840">Az.Batch</span></span>
- <span data-ttu-id="0e6b7-841">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-841">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0e6b7-842">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-842">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0e6b7-843">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0e6b7-844">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0e6b7-844">Az.Billing</span></span>
- <span data-ttu-id="0e6b7-845">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-845">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0e6b7-846">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-846">Az.CognitivServices</span></span>
- <span data-ttu-id="0e6b7-847">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-847">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0e6b7-848">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="0e6b7-848">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0e6b7-849">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-849">Az.ContainerInstance</span></span>
- <span data-ttu-id="0e6b7-850">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0e6b7-850">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0e6b7-851">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0e6b7-851">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0e6b7-852">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-852">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-853">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-853">Az.DataLakeStore</span></span>
- <span data-ttu-id="0e6b7-854">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-854">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0e6b7-855">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-855">Az.Monitor</span></span>
- <span data-ttu-id="0e6b7-856">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-856">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0e6b7-857">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e6b7-857">Az.KeyVault</span></span>
- <span data-ttu-id="0e6b7-858">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="0e6b7-858">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0e6b7-859">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0e6b7-859">Az.MachineLearning</span></span>
- <span data-ttu-id="0e6b7-860">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-860">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0e6b7-861">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0e6b7-861">Az.Media</span></span>
- <span data-ttu-id="0e6b7-862">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0e6b7-862">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0e6b7-863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-863">Az.Network</span></span>
<span data-ttu-id="0e6b7-864">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-864">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0e6b7-865">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-865">New cmdlets added:</span></span>
        - <span data-ttu-id="0e6b7-866">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-866">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-867">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-867">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-868">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-868">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-869">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-869">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-870">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-870">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-871">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-871">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0e6b7-872">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-872">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0e6b7-873">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6b7-873">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0e6b7-874">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-874">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0e6b7-875">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e6b7-875">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0e6b7-876">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-876">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0e6b7-877">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0e6b7-877">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0e6b7-878">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-878">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0e6b7-879">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-879">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0e6b7-880">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-880">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0e6b7-881">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e6b7-881">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0e6b7-882">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e6b7-882">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0e6b7-883">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e6b7-883">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0e6b7-884">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e6b7-884">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0e6b7-885">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0e6b7-885">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0e6b7-886">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-886">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0e6b7-887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-887">Az.OperationalInsights</span></span>
- <span data-ttu-id="0e6b7-888">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-888">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0e6b7-889">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-889">Az.Profile</span></span>
- <span data-ttu-id="0e6b7-890">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e6b7-890">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-891">Az.RecoveryServices</span></span>
- <span data-ttu-id="0e6b7-892">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0e6b7-893">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-893">Az.Resources</span></span>
- <span data-ttu-id="0e6b7-894">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-894">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-895">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-895">Az.ServiceFabric</span></span>
- <span data-ttu-id="0e6b7-896">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="0e6b7-896">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0e6b7-897">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-897">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0e6b7-898">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0e6b7-898">Az.SIgnalR</span></span>
- <span data-ttu-id="0e6b7-899">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0e6b7-899">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0e6b7-900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-900">Az.Sql</span></span>
- <span data-ttu-id="0e6b7-901">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="0e6b7-901">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0e6b7-902">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-902">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0e6b7-903">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-903">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0e6b7-904">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-904">Az.Storage</span></span>
- <span data-ttu-id="0e6b7-905">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0e6b7-906">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-906">Az.Websites</span></span>
- <span data-ttu-id="0e6b7-907">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0e6b7-907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0e6b7-908">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-908">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0e6b7-909">Ogólne</span><span class="sxs-lookup"><span data-stu-id="0e6b7-909">General</span></span>

* <span data-ttu-id="0e6b7-910">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="0e6b7-910">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0e6b7-911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-911">Az.Compute</span></span>

* <span data-ttu-id="0e6b7-912">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-912">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-913">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-913">Az.DataLakeStore</span></span>

* <span data-ttu-id="0e6b7-914">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="0e6b7-914">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0e6b7-915">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e6b7-915">Az.FrontDoor</span></span>

* <span data-ttu-id="0e6b7-916">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="0e6b7-916">Fixed some broken links</span></span>
    - <span data-ttu-id="0e6b7-917">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-917">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0e6b7-918">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-918">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0e6b7-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-919">Az.RecoveryServices</span></span>

* <span data-ttu-id="0e6b7-920">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-920">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0e6b7-921">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-921">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0e6b7-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-922">Az.Resources</span></span>

* <span data-ttu-id="0e6b7-923">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0e6b7-923">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0e6b7-924">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-924">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0e6b7-925">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-925">Az.Sql</span></span>

* <span data-ttu-id="0e6b7-926">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="0e6b7-926">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0e6b7-927">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="0e6b7-927">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0e6b7-928">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-928">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0e6b7-929">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-929">Az.Storage</span></span>

* <span data-ttu-id="0e6b7-930">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-930">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0e6b7-931">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="0e6b7-931">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0e6b7-932">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-932">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0e6b7-933">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-933">Support Static Website configuration</span></span>
    - <span data-ttu-id="0e6b7-934">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0e6b7-934">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0e6b7-935">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0e6b7-935">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0e6b7-936">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-936">Az.Websites</span></span>

* <span data-ttu-id="0e6b7-937">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e6b7-937">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0e6b7-938">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-938">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0e6b7-939">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-939">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0e6b7-940">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-940">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0e6b7-941">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e6b7-941">Az.ApiManagement</span></span>
* <span data-ttu-id="0e6b7-942">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-942">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0e6b7-943">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e6b7-943">Az.Automation</span></span>
* <span data-ttu-id="0e6b7-944">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="0e6b7-944">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0e6b7-945">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="0e6b7-945">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0e6b7-946">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="0e6b7-946">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0e6b7-947">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-947">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0e6b7-948">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="0e6b7-948">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0e6b7-949">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-949">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-950">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0e6b7-950">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0e6b7-951">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-951">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0e6b7-952">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-952">Az.ContainerInstance</span></span>
* <span data-ttu-id="0e6b7-953">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-953">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0e6b7-954">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0e6b7-954">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0e6b7-955">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="0e6b7-955">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0e6b7-956">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-956">Az.Network</span></span>
* <span data-ttu-id="0e6b7-957">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0e6b7-957">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0e6b7-958">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="0e6b7-958">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0e6b7-959">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-959">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0e6b7-960">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e6b7-960">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0e6b7-961">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0e6b7-961">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0e6b7-962">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-962">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0e6b7-963">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-963">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0e6b7-964">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0e6b7-964">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0e6b7-965">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e6b7-965">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0e6b7-966">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="0e6b7-966">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0e6b7-967">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0e6b7-967">Az.Relay</span></span>
* <span data-ttu-id="0e6b7-968">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-968">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0e6b7-969">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-969">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-970">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="0e6b7-970">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0e6b7-971">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="0e6b7-971">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0e6b7-972">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0e6b7-972">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-973">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-973">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e6b7-974">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="0e6b7-974">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0e6b7-975">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-975">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-976">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="0e6b7-976">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0e6b7-977">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-977">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e6b7-978">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-978">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e6b7-979">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-979">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e6b7-980">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e6b7-980">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e6b7-981">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e6b7-981">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e6b7-982">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e6b7-982">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e6b7-983">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e6b7-983">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e6b7-984">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e6b7-984">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0e6b7-985">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-985">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0e6b7-986">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-986">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0e6b7-987">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-987">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0e6b7-988">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-988">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0e6b7-989">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-989">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0e6b7-990">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-990">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0e6b7-991">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-991">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0e6b7-992">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="0e6b7-992">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0e6b7-993">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-993">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0e6b7-994">Ogólne</span><span class="sxs-lookup"><span data-stu-id="0e6b7-994">General</span></span>
* <span data-ttu-id="0e6b7-995">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-995">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0e6b7-996">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-996">Az.Profile</span></span>
* <span data-ttu-id="0e6b7-997">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="0e6b7-997">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0e6b7-998">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="0e6b7-998">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0e6b7-999">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0e6b7-999">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0e6b7-1000">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1000">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0e6b7-1001">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1001">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0e6b7-1002">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1002">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0e6b7-1003">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1003">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e6b7-1004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1004">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e6b7-1005">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1005">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-1006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1006">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-1007">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1007">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0e6b7-1008">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1008">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0e6b7-1009">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1009">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-1010">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1010">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-1011">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1011">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0e6b7-1012">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1012">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0e6b7-1013">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1013">Az.Insights</span></span>
* <span data-ttu-id="0e6b7-1014">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1014">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0e6b7-1015">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1015">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0e6b7-1016">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1016">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0e6b7-1017">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1017">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-1018">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1018">Az.Network</span></span>
* <span data-ttu-id="0e6b7-1019">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1019">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0e6b7-1020">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1020">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0e6b7-1021">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1021">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0e6b7-1022">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1022">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0e6b7-1023">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1023">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0e6b7-1024">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1024">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0e6b7-1025">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1025">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e6b7-1026">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1026">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e6b7-1027">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1027">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-1028">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1028">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-1029">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1029">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0e6b7-1030">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1030">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e6b7-1031">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1031">Az.ServiceBus</span></span>
* <span data-ttu-id="0e6b7-1032">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1032">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e6b7-1033">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1033">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e6b7-1034">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1034">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0e6b7-1035">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1035">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0e6b7-1036">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1036">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0e6b7-1037">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1037">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0e6b7-1038">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1038">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0e6b7-1039">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1039">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0e6b7-1040">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1040">Az.Profile</span></span>
* <span data-ttu-id="0e6b7-1041">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1041">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0e6b7-1042">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-1043">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1043">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-1044">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1044">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0e6b7-1045">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1045">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e6b7-1046">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1046">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e6b7-1047">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1047">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0e6b7-1048">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1048">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0e6b7-1049">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1049">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0e6b7-1050">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1050">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0e6b7-1051">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1051">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-1052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1052">Az.Network</span></span>
* <span data-ttu-id="0e6b7-1053">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1053">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0e6b7-1054">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1054">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-1055">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1055">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-1056">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1056">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0e6b7-1057">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1057">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0e6b7-1058">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1058">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0e6b7-1059">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1059">Azure.Storage</span></span>
* <span data-ttu-id="0e6b7-1060">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1060">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0e6b7-1061">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1061">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0e6b7-1062">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1062">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0e6b7-1063">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1063">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0e6b7-1064">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1064">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0e6b7-1065">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1065">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e6b7-1066">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1066">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e6b7-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1067">Az.Compute</span></span>
* <span data-ttu-id="0e6b7-1068">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1068">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0e6b7-1069">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1069">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0e6b7-1070">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1070">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0e6b7-1071">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1071">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0e6b7-1072">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1072">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e6b7-1073">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1073">Az.Network</span></span>
* <span data-ttu-id="0e6b7-1074">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1074">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0e6b7-1075">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1075">new cmdlets added</span></span>
    - <span data-ttu-id="0e6b7-1076">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1076">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e6b7-1077">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1077">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e6b7-1078">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1078">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e6b7-1079">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1079">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e6b7-1080">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1080">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0e6b7-1081">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1081">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0e6b7-1082">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1082">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0e6b7-1083">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1083">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0e6b7-1084">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1084">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e6b7-1085">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1085">Az.RedisCache</span></span>
* <span data-ttu-id="0e6b7-1086">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1086">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0e6b7-1087">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1087">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e6b7-1088">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1088">Az.Resources</span></span>
* <span data-ttu-id="0e6b7-1089">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1089">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0e6b7-1090">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1090">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e6b7-1091">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1091">Az.Sql</span></span>
* <span data-ttu-id="0e6b7-1092">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1092">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e6b7-1093">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1093">Az.Websites</span></span>
* <span data-ttu-id="0e6b7-1094">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1094">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0e6b7-1095">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1095">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0e6b7-1096">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1096">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0e6b7-1097">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="0e6b7-1097">Initial Release</span></span>