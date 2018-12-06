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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826735"
---
# <a name="release-notes"></a><span data-ttu-id="46632-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="46632-103">Release notes</span></span>

<span data-ttu-id="46632-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="46632-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="46632-105">6.13.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-106">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-107">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="46632-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46632-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46632-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46632-109">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="46632-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="46632-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="46632-110">AzureRM.Automation</span></span>
* <span data-ttu-id="46632-111">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="46632-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="46632-112">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="46632-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="46632-113">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="46632-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="46632-114">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="46632-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="46632-115">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="46632-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-116">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-117">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="46632-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="46632-118">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="46632-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="46632-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46632-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="46632-120">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="46632-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="46632-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46632-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="46632-122">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="46632-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-123">AzureRM.Network</span></span>
* <span data-ttu-id="46632-124">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="46632-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="46632-125">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="46632-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="46632-126">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="46632-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="46632-127">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46632-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46632-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46632-129">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="46632-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="46632-130">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="46632-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="46632-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46632-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46632-132">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="46632-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="46632-133">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="46632-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="46632-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="46632-134">AzureRM.Relay</span></span>
* <span data-ttu-id="46632-135">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="46632-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-136">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-137">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="46632-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="46632-138">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="46632-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="46632-139">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="46632-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46632-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46632-141">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="46632-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-142">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-143">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="46632-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="46632-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46632-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46632-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46632-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46632-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46632-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46632-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46632-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46632-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46632-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46632-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46632-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="46632-152">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="46632-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="46632-153">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="46632-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="46632-154">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="46632-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="46632-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46632-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46632-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46632-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46632-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46632-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="46632-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46632-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="46632-159">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="46632-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="46632-160">6.12.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-161">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-162">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="46632-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="46632-163">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzureRmAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="46632-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="46632-164">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="46632-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="46632-165">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="46632-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="46632-166">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="46632-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="46632-167">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="46632-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="46632-168">Rozwiązano problem polegający na zgłaszaniu elementu „Disconnect-AzureRmAccount” w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="46632-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="46632-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="46632-169">AzureRM.Automation</span></span>
* <span data-ttu-id="46632-170">Zmieniono nazwę biblioteki DLL polecenia cmdlet na Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="46632-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="46632-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46632-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="46632-172">Dodano operację Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="46632-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-173">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-174">Dodano polecenia cmdlet Add-AzureRmVmssVMDataDisk i Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46632-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="46632-175">Polecenie Get-AzureRmVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="46632-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="46632-176">Rozwiązano problem polegający na tym, że wartości opcji SetAzureRmVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="46632-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-178">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="46632-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="46632-179">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="46632-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="46632-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="46632-180">AzureRM.Insights</span></span>
* <span data-ttu-id="46632-181">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="46632-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="46632-182">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="46632-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="46632-183">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzureRMDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="46632-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="46632-184">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="46632-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-185">AzureRM.Network</span></span>
* <span data-ttu-id="46632-186">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="46632-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="46632-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="46632-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="46632-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="46632-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46632-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="46632-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="46632-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46632-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="46632-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46632-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46632-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="46632-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46632-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="46632-194">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="46632-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46632-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46632-196">Dodano obsługę udziałów plików platformy Azure do usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="46632-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-197">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-198">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="46632-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="46632-199">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="46632-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-201">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="46632-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46632-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46632-203">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="46632-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="46632-204">Rozwiązano problem z poleceniem „Add-AzureRmServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="46632-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="46632-205">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="46632-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="46632-206">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="46632-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="46632-207">Rozwiązano problem z poleceniem „Update-AzureRmServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="46632-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="46632-208">6.11.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-209">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-210">Rozwiązano problem z poleceniem Get-AzureRmSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="46632-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="46632-211">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="46632-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="46632-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-212">AzureRM.Backup</span></span>
* <span data-ttu-id="46632-213">Przestarzałe polecenia cmdlet usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="46632-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-214">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-215">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="46632-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="46632-216">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46632-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-218">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="46632-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="46632-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46632-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="46632-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46632-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46632-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46632-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46632-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46632-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-223">AzureRM.Network</span></span>
* <span data-ttu-id="46632-224">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="46632-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="46632-225">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46632-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-226">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-227">Rozwiązano problem polegający na tym, że polecenie Get-AzureRMRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="46632-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="46632-228">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="46632-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="46632-229">6.10.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="46632-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-230">Azure.Storage</span></span>
* <span data-ttu-id="46632-231">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="46632-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="46632-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46632-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="46632-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46632-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="46632-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46632-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="46632-235">Obsługa polecenia Get-AzureRmCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="46632-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-236">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-237">Rozwiązano problem z poleceniem Get-AzureRmVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="46632-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="46632-238">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="46632-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="46632-239">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="46632-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="46632-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46632-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="46632-241">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="46632-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-242">AzureRM.Network</span></span>
* <span data-ttu-id="46632-243">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="46632-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="46632-244">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="46632-244">new cmdlets added</span></span>
    - <span data-ttu-id="46632-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46632-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="46632-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46632-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="46632-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46632-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="46632-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46632-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="46632-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="46632-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="46632-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="46632-251">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="46632-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="46632-252">Dodano polecenia cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap i Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="46632-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="46632-253">Dodano polecenia cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig i Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="46632-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="46632-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46632-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="46632-255">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="46632-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="46632-256">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="46632-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-257">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-258">Dodano brakujący parametr -Mode do polecenia Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46632-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="46632-259">Usunięto błąd polecenia Get-AzureRmProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="46632-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-260">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-261">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="46632-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="46632-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-262">AzureRM.Storage</span></span>
* <span data-ttu-id="46632-263">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="46632-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="46632-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="46632-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-265">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-266">Nowe polecenie cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłe wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="46632-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="46632-267">Nowe polecenia cmdlet New-AzureRMWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="46632-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="46632-268">6.9.0 — wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46632-269">Ogólne</span><span class="sxs-lookup"><span data-stu-id="46632-269">General</span></span>
* <span data-ttu-id="46632-270">Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM</span><span class="sxs-lookup"><span data-stu-id="46632-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="46632-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-271">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-272">Drobne zmiany wspólnego kodu magazynu</span><span class="sxs-lookup"><span data-stu-id="46632-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="46632-273">Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.</span><span class="sxs-lookup"><span data-stu-id="46632-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="46632-274">Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46632-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="46632-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-275">Azure.Storage</span></span>
* <span data-ttu-id="46632-276">Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth.</span><span class="sxs-lookup"><span data-stu-id="46632-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="46632-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="46632-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="46632-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="46632-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="46632-279">Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="46632-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="46632-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-280">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-281">Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych</span><span class="sxs-lookup"><span data-stu-id="46632-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="46632-282">Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM</span><span class="sxs-lookup"><span data-stu-id="46632-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="46632-283">Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="46632-284">Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="46632-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="46632-285">Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="46632-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="46632-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="46632-286">AzureRM.Dns</span></span>
* <span data-ttu-id="46632-287">Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS</span><span class="sxs-lookup"><span data-stu-id="46632-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="46632-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="46632-288">AzureRM.Insights</span></span>
* <span data-ttu-id="46632-289">Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)</span><span class="sxs-lookup"><span data-stu-id="46632-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="46632-290">Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="46632-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="46632-291">Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii</span><span class="sxs-lookup"><span data-stu-id="46632-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="46632-292">Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk</span><span class="sxs-lookup"><span data-stu-id="46632-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="46632-293">Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa</span><span class="sxs-lookup"><span data-stu-id="46632-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-294">AzureRM.Network</span></span>
* <span data-ttu-id="46632-295">Zmiany poleceń cmdlet usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46632-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="46632-296">LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="46632-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="46632-297">LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="46632-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="46632-298">LoadBalancerRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="46632-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="46632-299">LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol</span><span class="sxs-lookup"><span data-stu-id="46632-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="46632-300">Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46632-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="46632-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46632-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="46632-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46632-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="46632-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46632-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="46632-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46632-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="46632-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46632-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="46632-306">Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="46632-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="46632-307">Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="46632-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="46632-308">Dodano polecenie Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="46632-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="46632-309">Dodano polecenie Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="46632-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="46632-310">Dodano polecenie New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="46632-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="46632-311">Dodano polecenie Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="46632-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="46632-312">Dodano polecenie New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46632-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="46632-313">Dodano polecenie New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="46632-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="46632-314">Dodano polecenie New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46632-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="46632-315">Dodano polecenie New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="46632-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="46632-316">Dodano polecenie New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46632-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="46632-317">Dodano polecenie New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46632-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="46632-318">Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="46632-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="46632-319">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="46632-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="46632-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="46632-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="46632-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="46632-329">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="46632-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46632-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="46632-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46632-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="46632-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="46632-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="46632-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="46632-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="46632-334">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="46632-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46632-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="46632-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46632-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="46632-337">Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="46632-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="46632-338">Dodano obsługę wielu prefiksów adresów w podsieci.</span><span class="sxs-lookup"><span data-stu-id="46632-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="46632-339">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="46632-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46632-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="46632-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46632-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="46632-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46632-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="46632-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46632-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="46632-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="46632-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="46632-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="46632-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="46632-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="46632-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="46632-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="46632-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="46632-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="46632-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="46632-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="46632-352">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="46632-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="46632-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="46632-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="46632-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="46632-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="46632-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="46632-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="46632-359">Dodano polecenia cmdlet na potrzeby delegowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="46632-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="46632-360">New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci</span><span class="sxs-lookup"><span data-stu-id="46632-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="46632-361">Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania</span><span class="sxs-lookup"><span data-stu-id="46632-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="46632-362">Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie</span><span class="sxs-lookup"><span data-stu-id="46632-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="46632-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="46632-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="46632-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="46632-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="46632-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46632-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46632-366">Obsługa dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="46632-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="46632-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46632-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="46632-368">Zaktualizowano zależność szczegółowych informacji.</span><span class="sxs-lookup"><span data-stu-id="46632-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-369">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-370">Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction</span><span class="sxs-lookup"><span data-stu-id="46632-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="46632-371">Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.</span><span class="sxs-lookup"><span data-stu-id="46632-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="46632-372">Obsługa tożsamości zarządzanej w przypisaniach zasad.</span><span class="sxs-lookup"><span data-stu-id="46632-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="46632-373">Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="46632-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="46632-374">Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad</span><span class="sxs-lookup"><span data-stu-id="46632-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-376">Rozwiązano problem nr 7161</span><span class="sxs-lookup"><span data-stu-id="46632-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="46632-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="46632-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="46632-378">Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1</span><span class="sxs-lookup"><span data-stu-id="46632-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="46632-379">Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="46632-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="46632-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-380">AzureRM.Storage</span></span>
* <span data-ttu-id="46632-381">Obsługa zasad niezmienności w elemencie AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="46632-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46632-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="46632-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46632-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="46632-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46632-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="46632-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46632-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="46632-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46632-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="46632-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="46632-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="46632-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="46632-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="46632-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="46632-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="46632-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="46632-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-393">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-394">Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="46632-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="46632-395">New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="46632-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="46632-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią</span><span class="sxs-lookup"><span data-stu-id="46632-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="46632-397">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46632-398">Ogólne</span><span class="sxs-lookup"><span data-stu-id="46632-398">General</span></span>
* <span data-ttu-id="46632-399">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="46632-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="46632-400">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="46632-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46632-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46632-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46632-402">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="46632-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="46632-403">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="46632-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="46632-404">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="46632-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="46632-405">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="46632-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="46632-406">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="46632-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="46632-407">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="46632-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="46632-408">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="46632-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="46632-409">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="46632-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="46632-410">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="46632-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="46632-411">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="46632-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="46632-412">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="46632-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="46632-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-413">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-414">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="46632-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="46632-415">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="46632-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="46632-416">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="46632-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="46632-417">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="46632-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-418">AzureRM.Network</span></span>
* <span data-ttu-id="46632-419">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="46632-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="46632-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46632-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="46632-421">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="46632-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="46632-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-422">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-423">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="46632-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-425">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="46632-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46632-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46632-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46632-427">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="46632-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="46632-428">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="46632-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="46632-429">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="46632-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="46632-430">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="46632-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="46632-431">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="46632-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="46632-432">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="46632-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="46632-433">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="46632-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="46632-434">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46632-435">Ogólne</span><span class="sxs-lookup"><span data-stu-id="46632-435">General</span></span>
* <span data-ttu-id="46632-436">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="46632-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="46632-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-437">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-438">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="46632-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-439">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-440">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="46632-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="46632-441">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="46632-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="46632-442">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="46632-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="46632-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="46632-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="46632-444">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="46632-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-445">AzureRM.Network</span></span>
* <span data-ttu-id="46632-446">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="46632-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="46632-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46632-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="46632-448">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="46632-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-449">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-450">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="46632-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-452">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="46632-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46632-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46632-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46632-454">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="46632-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="46632-455">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="46632-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="46632-456">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="46632-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="46632-457">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="46632-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="46632-458">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="46632-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="46632-459">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="46632-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="46632-460">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="46632-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-461">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-462">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="46632-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="46632-463">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-464">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-465">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="46632-466">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="46632-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="46632-467">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="46632-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="46632-468">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="46632-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="46632-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-469">Azure.Storage</span></span>
* <span data-ttu-id="46632-470">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="46632-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="46632-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="46632-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="46632-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46632-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="46632-473">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="46632-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46632-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="46632-475">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46632-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46632-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46632-477">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="46632-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="46632-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="46632-479">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="46632-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="46632-480">AzureRM.Automation</span></span>
* <span data-ttu-id="46632-481">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="46632-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-482">AzureRM.Backup</span></span>
* <span data-ttu-id="46632-483">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="46632-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="46632-484">AzureRM.Batch</span></span>
* <span data-ttu-id="46632-485">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="46632-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="46632-486">AzureRM.Billing</span></span>
* <span data-ttu-id="46632-487">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="46632-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="46632-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="46632-489">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="46632-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46632-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="46632-491">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-492">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-493">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="46632-494">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="46632-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="46632-495">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="46632-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="46632-496">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="46632-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="46632-497">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="46632-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="46632-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="46632-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="46632-499">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="46632-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46632-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="46632-501">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="46632-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46632-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="46632-503">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="46632-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="46632-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="46632-505">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="46632-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46632-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="46632-507">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="46632-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46632-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="46632-509">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-511">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="46632-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="46632-512">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="46632-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="46632-513">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="46632-514">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="46632-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="46632-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="46632-516">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="46632-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="46632-517">AzureRM.Dns</span></span>
* <span data-ttu-id="46632-518">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="46632-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46632-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="46632-520">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46632-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46632-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="46632-522">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="46632-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46632-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="46632-524">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="46632-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="46632-525">AzureRM.Insights</span></span>
* <span data-ttu-id="46632-526">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="46632-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="46632-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="46632-528">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46632-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-530">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="46632-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46632-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="46632-532">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="46632-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46632-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="46632-534">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="46632-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="46632-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="46632-536">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="46632-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46632-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="46632-538">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="46632-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="46632-539">AzureRM.Media</span></span>
* <span data-ttu-id="46632-540">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-541">AzureRM.Network</span></span>
* <span data-ttu-id="46632-542">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46632-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="46632-543">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46632-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46632-544">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46632-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="46632-545">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="46632-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="46632-546">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="46632-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="46632-547">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46632-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46632-548">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="46632-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="46632-549">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="46632-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="46632-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="46632-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="46632-551">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="46632-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46632-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="46632-553">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="46632-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46632-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="46632-555">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="46632-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46632-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="46632-557">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="46632-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46632-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="46632-559">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46632-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46632-561">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="46632-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="46632-562">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="46632-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="46632-563">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="46632-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="46632-564">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="46632-565">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="46632-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="46632-566">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="46632-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="46632-567">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="46632-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="46632-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46632-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46632-569">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="46632-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46632-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="46632-571">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="46632-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="46632-572">AzureRM.Relay</span></span>
* <span data-ttu-id="46632-573">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-574">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-575">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46632-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="46632-576">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="46632-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="46632-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="46632-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="46632-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="46632-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="46632-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="46632-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="46632-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="46632-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="46632-584">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="46632-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="46632-585">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="46632-586">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="46632-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="46632-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="46632-588">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-590">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46632-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46632-592">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-593">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-594">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="46632-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-595">AzureRM.Storage</span></span>
* <span data-ttu-id="46632-596">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="46632-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="46632-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="46632-598">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="46632-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="46632-599">AzureRM.Tags</span></span>
* <span data-ttu-id="46632-600">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46632-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46632-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46632-602">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="46632-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="46632-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="46632-604">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-605">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-606">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="46632-607">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46632-608">Ogólne</span><span class="sxs-lookup"><span data-stu-id="46632-608">General</span></span>
* <span data-ttu-id="46632-609">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="46632-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="46632-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-610">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-611">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="46632-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="46632-612">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="46632-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-613">Azure.Storage</span></span>
* <span data-ttu-id="46632-614">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46632-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="46632-615">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46632-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46632-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46632-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46632-617">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="46632-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="46632-618">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="46632-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="46632-619">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="46632-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="46632-620">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="46632-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="46632-621">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="46632-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="46632-622">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="46632-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-623">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-624">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="46632-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="46632-625">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="46632-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="46632-626">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46632-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="46632-627">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="46632-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="46632-628">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="46632-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="46632-629">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="46632-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="46632-630">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="46632-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="46632-631">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="46632-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="46632-632">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="46632-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="46632-633">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="46632-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="46632-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46632-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="46632-635">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="46632-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="46632-636">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="46632-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="46632-637">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="46632-638">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="46632-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-640">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="46632-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46632-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46632-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="46632-642">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="46632-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="46632-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="46632-643">AzureRM.Insights</span></span>
* <span data-ttu-id="46632-644">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="46632-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="46632-645">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="46632-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46632-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-647">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-648">AzureRM.Network</span></span>
* <span data-ttu-id="46632-649">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="46632-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-650">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-651">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="46632-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="46632-652">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="46632-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-654">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="46632-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="46632-655">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="46632-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="46632-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-656">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-657">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="46632-658">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="46632-659">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="46632-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="46632-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="46632-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="46632-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="46632-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="46632-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="46632-663">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="46632-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="46632-664">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="46632-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="46632-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-665">AzureRM.Storage</span></span>
* <span data-ttu-id="46632-666">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="46632-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="46632-667">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="46632-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="46632-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46632-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="46632-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46632-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="46632-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46632-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="46632-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="46632-671">AzureRM.Tags</span></span>
* <span data-ttu-id="46632-672">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="46632-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="46632-673">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-674">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-675">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="46632-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="46632-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-676">Azure.Storage</span></span>
* <span data-ttu-id="46632-677">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="46632-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="46632-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46632-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="46632-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46632-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="46632-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46632-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="46632-681">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="46632-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="46632-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="46632-682">AzureRM.Automation</span></span>
* <span data-ttu-id="46632-683">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="46632-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-684">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-685">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="46632-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="46632-686">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="46632-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="46632-687">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="46632-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="46632-688">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="46632-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="46632-689">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="46632-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46632-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46632-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="46632-691">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="46632-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46632-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-693">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="46632-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="46632-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46632-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="46632-695">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="46632-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-696">AzureRM.Network</span></span>
* <span data-ttu-id="46632-697">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="46632-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="46632-698">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="46632-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="46632-699">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="46632-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="46632-700">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="46632-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="46632-701">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="46632-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="46632-702">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="46632-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="46632-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="46632-703">AzureRM.Relay</span></span>
* <span data-ttu-id="46632-704">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="46632-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-705">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-706">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="46632-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="46632-707">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="46632-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="46632-708">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="46632-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="46632-709">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="46632-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="46632-710">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="46632-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-712">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="46632-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="46632-713">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="46632-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="46632-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46632-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46632-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46632-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46632-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46632-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46632-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46632-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46632-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46632-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="46632-719">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="46632-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46632-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46632-721">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="46632-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-722">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-723">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="46632-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="46632-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="46632-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-726">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-727">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="46632-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="46632-728">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="46632-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="46632-729">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="46632-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="46632-730">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46632-731">Ogólne</span><span class="sxs-lookup"><span data-stu-id="46632-731">General</span></span>
* <span data-ttu-id="46632-732">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="46632-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="46632-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-733">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-734">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="46632-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-735">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-736">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="46632-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="46632-737">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="46632-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="46632-738">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="46632-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="46632-739">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="46632-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="46632-740">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="46632-741">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="46632-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="46632-742">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="46632-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46632-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="46632-744">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="46632-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="46632-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="46632-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="46632-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-749">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="46632-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="46632-750">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="46632-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="46632-751">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="46632-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="46632-752">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="46632-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46632-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46632-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="46632-754">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="46632-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="46632-755">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="46632-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="46632-756">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="46632-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="46632-757">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="46632-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46632-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-759">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="46632-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-760">AzureRM.Network</span></span>
* <span data-ttu-id="46632-761">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="46632-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="46632-762">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="46632-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="46632-763">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="46632-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="46632-764">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="46632-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="46632-765">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="46632-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46632-766">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="46632-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46632-767">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="46632-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46632-768">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="46632-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46632-769">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="46632-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46632-770">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46632-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46632-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46632-772">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="46632-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="46632-773">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46632-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="46632-774">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="46632-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-775">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-776">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="46632-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="46632-777">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="46632-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="46632-778">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="46632-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="46632-779">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="46632-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="46632-780">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46632-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="46632-781">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="46632-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="46632-782">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46632-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="46632-783">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="46632-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="46632-784">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="46632-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="46632-785">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46632-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="46632-786">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="46632-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="46632-787">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="46632-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="46632-788">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="46632-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="46632-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46632-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46632-790">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="46632-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-791">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-792">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="46632-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="46632-793">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="46632-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="46632-794">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="46632-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-795">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-796">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="46632-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="46632-797">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="46632-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="46632-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46632-798">Azure.Storage</span></span>
* <span data-ttu-id="46632-799">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="46632-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-800">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-801">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="46632-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="46632-802">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46632-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="46632-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="46632-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="46632-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="46632-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="46632-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="46632-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="46632-806">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="46632-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="46632-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46632-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="46632-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46632-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="46632-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46632-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="46632-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46632-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="46632-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="46632-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="46632-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="46632-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="46632-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="46632-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="46632-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="46632-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="46632-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="46632-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="46632-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46632-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="46632-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="46632-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="46632-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="46632-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="46632-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="46632-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="46632-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="46632-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="46632-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="46632-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="46632-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46632-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="46632-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="46632-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="46632-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46632-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="46632-827">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="46632-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46632-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-829">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="46632-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="46632-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46632-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="46632-831">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="46632-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="46632-832">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="46632-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="46632-833">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="46632-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46632-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46632-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46632-835">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="46632-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="46632-836">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="46632-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-837">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-838">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="46632-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46632-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46632-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46632-840">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="46632-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-841">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-842">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="46632-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="46632-843">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="46632-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="46632-844">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="46632-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="46632-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46632-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="46632-846">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="46632-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="46632-847">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="46632-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-848">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-849">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="46632-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46632-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46632-850">AzureRM.Compute</span></span>
* <span data-ttu-id="46632-851">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="46632-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="46632-852">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="46632-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="46632-853">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="46632-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="46632-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46632-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="46632-855">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="46632-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="46632-856">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="46632-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="46632-857">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="46632-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="46632-858">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="46632-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="46632-859">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="46632-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="46632-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46632-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46632-861">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="46632-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="46632-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-862">AzureRM.Network</span></span>
* <span data-ttu-id="46632-863">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="46632-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46632-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46632-864">AzureRM.Resources</span></span>
* <span data-ttu-id="46632-865">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="46632-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="46632-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="46632-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="46632-867">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="46632-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="46632-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-868">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-869">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="46632-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="46632-870">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="46632-871">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46632-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="46632-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="46632-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="46632-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46632-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="46632-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46632-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46632-875">AzureRM.Websites</span></span>
* <span data-ttu-id="46632-876">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="46632-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="46632-877">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="46632-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46632-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46632-878">AzureRM.Profile</span></span>
* <span data-ttu-id="46632-879">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="46632-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="46632-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46632-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="46632-881">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="46632-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46632-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46632-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46632-883">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="46632-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="46632-884">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="46632-885">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="46632-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="46632-886">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="46632-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="46632-887">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="46632-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="46632-888">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="46632-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="46632-889">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="46632-889">Added support for MSI identity</span></span>
* <span data-ttu-id="46632-890">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="46632-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="46632-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="46632-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="46632-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="46632-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="46632-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="46632-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="46632-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="46632-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="46632-895">AzureRM.Batch</span></span>
* <span data-ttu-id="46632-896">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="46632-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="46632-897">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="46632-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="46632-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="46632-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="46632-899">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="46632-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46632-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46632-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46632-901">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="46632-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="46632-902">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="46632-903">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46632-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="46632-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46632-904">AzureRM.Network</span></span>
* <span data-ttu-id="46632-905">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="46632-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="46632-906">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="46632-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="46632-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="46632-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="46632-908">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="46632-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="46632-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46632-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="46632-910">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="46632-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="46632-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46632-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="46632-912">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="46632-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="46632-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46632-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46632-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46632-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46632-915">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="46632-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46632-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46632-916">AzureRM.Sql</span></span>
* <span data-ttu-id="46632-917">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="46632-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="46632-918">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="46632-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="46632-919">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="46632-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="46632-920">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="46632-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="46632-921">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="46632-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="46632-922">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="46632-923">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46632-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="46632-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="46632-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="46632-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46632-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="46632-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46632-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46632-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46632-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46632-928">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="46632-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
