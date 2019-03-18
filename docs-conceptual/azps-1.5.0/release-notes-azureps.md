---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882476"
---
## <a name="150---march-2019"></a><span data-ttu-id="2d48c-101">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="2d48c-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d48c-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-102">Az.Accounts</span></span>
* <span data-ttu-id="2d48c-103">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="2d48c-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2d48c-104">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d48c-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d48c-105">Az.Automation</span></span>
* <span data-ttu-id="2d48c-106">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="2d48c-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d48c-107">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="2d48c-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2d48c-108">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="2d48c-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d48c-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d48c-109">Az.Cdn</span></span>
* <span data-ttu-id="2d48c-110">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="2d48c-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-111">Az.Compute</span></span>
* <span data-ttu-id="2d48c-112">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="2d48c-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d48c-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d48c-113">Az.DataFactory</span></span>
* <span data-ttu-id="2d48c-114">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2d48c-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d48c-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d48c-115">Az.LogicApp</span></span>
* <span data-ttu-id="2d48c-116">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="2d48c-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-117">Az.Network</span></span>
* <span data-ttu-id="2d48c-118">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="2d48c-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d48c-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d48c-120">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d48c-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2d48c-121">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="2d48c-121">SDK Update</span></span>
* <span data-ttu-id="2d48c-122">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d48c-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2d48c-123">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d48c-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-124">Az.Resources</span></span>
* <span data-ttu-id="2d48c-125">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="2d48c-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2d48c-126">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2d48c-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2d48c-127">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2d48c-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2d48c-128">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2d48c-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2d48c-129">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2d48c-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2d48c-130">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2d48c-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-131">Az.Sql</span></span>
* <span data-ttu-id="2d48c-132">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2d48c-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2d48c-133">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="2d48c-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d48c-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-134">Az.Storage</span></span>
* <span data-ttu-id="2d48c-135">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2d48c-136">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2d48c-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d48c-138">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d48c-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d48c-139">Az.Automation</span></span>
* <span data-ttu-id="2d48c-140">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2d48c-141">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2d48c-142">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d48c-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d48c-144">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="2d48c-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-145">Az.Compute</span></span>
* <span data-ttu-id="2d48c-146">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="2d48c-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2d48c-147">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="2d48c-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2d48c-148">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d48c-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2d48c-149">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="2d48c-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d48c-151">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="2d48c-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d48c-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d48c-152">Az.EventHub</span></span>
* <span data-ttu-id="2d48c-153">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="2d48c-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2d48c-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d48c-154">Az.KeyVault</span></span>
* <span data-ttu-id="2d48c-155">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d48c-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d48c-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d48c-156">Az.LogicApp</span></span>
* <span data-ttu-id="2d48c-157">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="2d48c-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2d48c-158">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="2d48c-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2d48c-159">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="2d48c-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2d48c-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d48c-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d48c-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d48c-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d48c-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d48c-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d48c-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d48c-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2d48c-164">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="2d48c-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2d48c-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d48c-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d48c-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d48c-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2d48c-169">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2d48c-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d48c-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d48c-170">Az.Monitor</span></span>
* <span data-ttu-id="2d48c-171">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="2d48c-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-172">Az.Network</span></span>
* <span data-ttu-id="2d48c-173">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2d48c-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d48c-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d48c-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d48c-175">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2d48c-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2d48c-176">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2d48c-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2d48c-177">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="2d48c-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2d48c-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-178">Az.Resources</span></span>
* <span data-ttu-id="2d48c-179">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d48c-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d48c-180">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d48c-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2d48c-181">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2d48c-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2d48c-182">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2d48c-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-183">Az.Sql</span></span>
* <span data-ttu-id="2d48c-184">Dodano obsługę warstwy bazy danych SQL w hiperskali</span><span class="sxs-lookup"><span data-stu-id="2d48c-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2d48c-185">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="2d48c-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d48c-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-186">Az.Websites</span></span>
* <span data-ttu-id="2d48c-187">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2d48c-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2d48c-188">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d48c-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-189">Az.Accounts</span></span>
* <span data-ttu-id="2d48c-190">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d48c-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d48c-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-191">Az.AnalysisServices</span></span>
<span data-ttu-id="2d48c-192">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2d48c-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-193">Az.Compute</span></span>
* <span data-ttu-id="2d48c-194">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="2d48c-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2d48c-195">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2d48c-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2d48c-196">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d48c-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d48c-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-197">Az.RecoveryServices</span></span>
<span data-ttu-id="2d48c-198">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2d48c-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-199">Az.Resources</span></span>
* <span data-ttu-id="2d48c-200">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="2d48c-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2d48c-201">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d48c-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d48c-202">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2d48c-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2d48c-203">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d48c-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-204">Az.Sql</span></span>
* <span data-ttu-id="2d48c-205">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d48c-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2d48c-206">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="2d48c-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2d48c-207">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2d48c-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2d48c-208">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d48c-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-209">Az.Accounts</span></span>
* <span data-ttu-id="2d48c-210">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="2d48c-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d48c-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d48c-212">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="2d48c-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d48c-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d48c-214">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="2d48c-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2d48c-215">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d48c-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-216">Az.Accounts</span></span>
* <span data-ttu-id="2d48c-217">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d48c-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d48c-218">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d48c-219">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2d48c-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d48c-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d48c-220">Az.Aks</span></span>
* <span data-ttu-id="2d48c-221">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d48c-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d48c-222">Az.Automation</span></span>
* <span data-ttu-id="2d48c-223">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="2d48c-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2d48c-224">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d48c-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d48c-225">Az.Cdn</span></span>
* <span data-ttu-id="2d48c-226">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-227">Az.Compute</span></span>
* <span data-ttu-id="2d48c-228">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2d48c-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2d48c-229">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d48c-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2d48c-230">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d48c-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d48c-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d48c-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d48c-232">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d48c-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d48c-233">Az.DataFactory</span></span>
* <span data-ttu-id="2d48c-234">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2d48c-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d48c-236">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="2d48c-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2d48c-237">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2d48c-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2d48c-238">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d48c-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d48c-239">Az.IotHub</span></span>
* <span data-ttu-id="2d48c-240">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d48c-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d48c-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d48c-241">Az.KeyVault</span></span>
* <span data-ttu-id="2d48c-242">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-243">Az.Network</span></span>
* <span data-ttu-id="2d48c-244">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-245">Az.Resources</span></span>
* <span data-ttu-id="2d48c-246">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2d48c-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2d48c-247">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2d48c-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2d48c-248">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d48c-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2d48c-249">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2d48c-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2d48c-250">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2d48c-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2d48c-251">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d48c-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2d48c-252">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2d48c-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d48c-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d48c-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d48c-254">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2d48c-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2d48c-255">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="2d48c-255">Fix some error messages.</span></span>
* <span data-ttu-id="2d48c-256">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d48c-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2d48c-257">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="2d48c-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d48c-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d48c-258">Az.SignalR</span></span>
* <span data-ttu-id="2d48c-259">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-260">Az.Sql</span></span>
* <span data-ttu-id="2d48c-261">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d48c-262">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="2d48c-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2d48c-263">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="2d48c-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2d48c-264">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="2d48c-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d48c-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-265">Az.Storage</span></span>
* <span data-ttu-id="2d48c-266">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d48c-267">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="2d48c-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2d48c-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2d48c-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2d48c-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2d48c-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d48c-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d48c-270">Az.TrafficManager</span></span>
* <span data-ttu-id="2d48c-271">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d48c-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-272">Az.Websites</span></span>
* <span data-ttu-id="2d48c-273">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="2d48c-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d48c-274">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="2d48c-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2d48c-275">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="2d48c-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2d48c-276">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d48c-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-277">Az.Accounts</span></span>
* <span data-ttu-id="2d48c-278">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2d48c-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-279">Az.Compute</span></span>
* <span data-ttu-id="2d48c-280">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2d48c-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2d48c-281">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="2d48c-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2d48c-282">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d48c-284">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="2d48c-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2d48c-285">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="2d48c-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d48c-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d48c-286">Az.EventGrid</span></span>
* <span data-ttu-id="2d48c-287">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d48c-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2d48c-288">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2d48c-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2d48c-289">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="2d48c-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d48c-290">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="2d48c-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d48c-291">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="2d48c-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d48c-292">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="2d48c-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2d48c-293">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="2d48c-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d48c-294">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="2d48c-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d48c-295">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="2d48c-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d48c-296">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="2d48c-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="2d48c-297">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d48c-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2d48c-298">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2d48c-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d48c-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d48c-299">Az.IotHub</span></span>
* <span data-ttu-id="2d48c-300">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="2d48c-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d48c-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d48c-301">Az.LogicApp</span></span>
* <span data-ttu-id="2d48c-302">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="2d48c-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-303">Az.Resources</span></span>
* <span data-ttu-id="2d48c-304">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="2d48c-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2d48c-305">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2d48c-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2d48c-306">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d48c-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d48c-307">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2d48c-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2d48c-308">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="2d48c-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2d48c-309">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2d48c-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d48c-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d48c-310">Az.SignalR</span></span>
* <span data-ttu-id="2d48c-311">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-312">Az.Sql</span></span>
* <span data-ttu-id="2d48c-313">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="2d48c-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d48c-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-314">Az.Storage</span></span>
* <span data-ttu-id="2d48c-315">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="2d48c-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2d48c-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d48c-316">New-AzStorageContext</span></span>
* <span data-ttu-id="2d48c-317">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="2d48c-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2d48c-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d48c-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d48c-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-319">Az.Websites</span></span>
* <span data-ttu-id="2d48c-320">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="2d48c-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d48c-321">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2d48c-322">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2d48c-323">Ogólne</span><span class="sxs-lookup"><span data-stu-id="2d48c-323">General</span></span>

- <span data-ttu-id="2d48c-324">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="2d48c-324">General Availability of Az Module</span></span>
- <span data-ttu-id="2d48c-325">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="2d48c-325">Online help for each module</span></span>
- <span data-ttu-id="2d48c-326">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2d48c-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2d48c-327">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="2d48c-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2d48c-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-328">Az.Accounts</span></span>
- <span data-ttu-id="2d48c-329">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d48c-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="2d48c-330">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="2d48c-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d48c-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d48c-331">Az.ApiManagement</span></span>
- <span data-ttu-id="2d48c-332">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="2d48c-332">Fixes for #7002</span></span>
- <span data-ttu-id="2d48c-333">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2d48c-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d48c-334">Az.Batch</span></span>
- <span data-ttu-id="2d48c-335">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2d48c-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2d48c-336">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="2d48c-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2d48c-337">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2d48c-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d48c-338">Az.Billing</span></span>
- <span data-ttu-id="2d48c-339">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2d48c-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-340">Az.CognitivServices</span></span>
- <span data-ttu-id="2d48c-341">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2d48c-342">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2d48c-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d48c-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="2d48c-344">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d48c-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2d48c-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d48c-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2d48c-346">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="2d48c-348">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2d48c-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d48c-349">Az.Monitor</span></span>
- <span data-ttu-id="2d48c-350">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2d48c-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d48c-351">Az.KeyVault</span></span>
- <span data-ttu-id="2d48c-352">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2d48c-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2d48c-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d48c-353">Az.MachineLearning</span></span>
- <span data-ttu-id="2d48c-354">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2d48c-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2d48c-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d48c-355">Az.Media</span></span>
- <span data-ttu-id="2d48c-356">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d48c-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d48c-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-357">Az.Network</span></span>
<span data-ttu-id="2d48c-358">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2d48c-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2d48c-359">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d48c-359">New cmdlets added:</span></span>
        - <span data-ttu-id="2d48c-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2d48c-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2d48c-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2d48c-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d48c-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2d48c-368">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d48c-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2d48c-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d48c-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2d48c-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d48c-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d48c-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d48c-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d48c-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d48c-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2d48c-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d48c-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2d48c-374">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2d48c-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2d48c-375">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d48c-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2d48c-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d48c-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d48c-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d48c-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d48c-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d48c-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2d48c-379">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d48c-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2d48c-380">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2d48c-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d48c-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="2d48c-382">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2d48c-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d48c-383">Az.Profile</span></span>
- <span data-ttu-id="2d48c-384">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d48c-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d48c-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="2d48c-386">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2d48c-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-387">Az.Resources</span></span>
- <span data-ttu-id="2d48c-388">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d48c-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d48c-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="2d48c-390">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="2d48c-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2d48c-391">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2d48c-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d48c-392">Az.SIgnalR</span></span>
- <span data-ttu-id="2d48c-393">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d48c-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2d48c-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-394">Az.Sql</span></span>
- <span data-ttu-id="2d48c-395">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="2d48c-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2d48c-396">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="2d48c-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2d48c-397">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d48c-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-398">Az.Storage</span></span>
- <span data-ttu-id="2d48c-399">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d48c-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-400">Az.Websites</span></span>
- <span data-ttu-id="2d48c-401">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="2d48c-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2d48c-402">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2d48c-403">Ogólne</span><span class="sxs-lookup"><span data-stu-id="2d48c-403">General</span></span>

* <span data-ttu-id="2d48c-404">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="2d48c-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d48c-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-405">Az.Compute</span></span>

* <span data-ttu-id="2d48c-406">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2d48c-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="2d48c-408">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="2d48c-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2d48c-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d48c-409">Az.FrontDoor</span></span>

* <span data-ttu-id="2d48c-410">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="2d48c-410">Fixed some broken links</span></span>
    - <span data-ttu-id="2d48c-411">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2d48c-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2d48c-412">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2d48c-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d48c-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="2d48c-414">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d48c-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2d48c-415">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d48c-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d48c-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-416">Az.Resources</span></span>

* <span data-ttu-id="2d48c-417">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2d48c-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2d48c-418">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="2d48c-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2d48c-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-419">Az.Sql</span></span>

* <span data-ttu-id="2d48c-420">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="2d48c-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2d48c-421">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="2d48c-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2d48c-422">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="2d48c-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d48c-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-423">Az.Storage</span></span>

* <span data-ttu-id="2d48c-424">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2d48c-425">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="2d48c-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2d48c-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d48c-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d48c-427">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="2d48c-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="2d48c-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d48c-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2d48c-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d48c-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d48c-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-430">Az.Websites</span></span>

* <span data-ttu-id="2d48c-431">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d48c-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2d48c-432">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="2d48c-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2d48c-433">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2d48c-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2d48c-434">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d48c-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d48c-435">Az.ApiManagement</span></span>
* <span data-ttu-id="2d48c-436">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="2d48c-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2d48c-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d48c-437">Az.Automation</span></span>
* <span data-ttu-id="2d48c-438">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="2d48c-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d48c-439">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="2d48c-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2d48c-440">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="2d48c-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2d48c-441">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="2d48c-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2d48c-442">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="2d48c-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d48c-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-443">Az.Compute</span></span>
* <span data-ttu-id="2d48c-444">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2d48c-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2d48c-445">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="2d48c-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d48c-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d48c-447">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="2d48c-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2d48c-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d48c-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d48c-449">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="2d48c-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d48c-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-450">Az.Network</span></span>
* <span data-ttu-id="2d48c-451">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2d48c-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2d48c-452">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2d48c-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2d48c-453">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="2d48c-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2d48c-454">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d48c-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2d48c-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d48c-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d48c-456">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2d48c-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2d48c-457">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="2d48c-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2d48c-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d48c-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2d48c-459">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d48c-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2d48c-460">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="2d48c-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2d48c-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d48c-461">Az.Relay</span></span>
* <span data-ttu-id="2d48c-462">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2d48c-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d48c-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-463">Az.Resources</span></span>
* <span data-ttu-id="2d48c-464">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2d48c-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2d48c-465">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="2d48c-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2d48c-466">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2d48c-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d48c-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d48c-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d48c-468">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="2d48c-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2d48c-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-469">Az.Sql</span></span>
* <span data-ttu-id="2d48c-470">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="2d48c-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2d48c-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d48c-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d48c-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d48c-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d48c-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d48c-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d48c-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d48c-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d48c-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d48c-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d48c-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d48c-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d48c-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2d48c-479">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="2d48c-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2d48c-480">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="2d48c-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2d48c-481">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="2d48c-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2d48c-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d48c-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d48c-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d48c-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d48c-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d48c-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2d48c-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d48c-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2d48c-486">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2d48c-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2d48c-487">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d48c-488">Ogólne</span><span class="sxs-lookup"><span data-stu-id="2d48c-488">General</span></span>
* <span data-ttu-id="2d48c-489">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d48c-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2d48c-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d48c-490">Az.Profile</span></span>
* <span data-ttu-id="2d48c-491">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="2d48c-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2d48c-492">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="2d48c-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2d48c-493">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d48c-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2d48c-494">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="2d48c-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2d48c-495">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="2d48c-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2d48c-496">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="2d48c-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2d48c-497">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="2d48c-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d48c-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d48c-499">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2d48c-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-500">Az.Compute</span></span>
* <span data-ttu-id="2d48c-501">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d48c-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2d48c-502">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2d48c-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2d48c-503">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="2d48c-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d48c-505">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2d48c-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2d48c-506">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="2d48c-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2d48c-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2d48c-507">Az.Insights</span></span>
* <span data-ttu-id="2d48c-508">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="2d48c-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2d48c-509">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="2d48c-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2d48c-510">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="2d48c-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2d48c-511">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="2d48c-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-512">Az.Network</span></span>
* <span data-ttu-id="2d48c-513">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d48c-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2d48c-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d48c-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2d48c-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2d48c-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2d48c-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d48c-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2d48c-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d48c-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d48c-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d48c-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d48c-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d48c-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d48c-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d48c-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d48c-521">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="2d48c-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-522">Az.Resources</span></span>
* <span data-ttu-id="2d48c-523">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2d48c-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2d48c-524">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="2d48c-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d48c-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d48c-525">Az.ServiceBus</span></span>
* <span data-ttu-id="2d48c-526">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="2d48c-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d48c-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d48c-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d48c-528">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="2d48c-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2d48c-529">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="2d48c-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2d48c-530">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2d48c-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2d48c-531">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2d48c-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2d48c-532">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="2d48c-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2d48c-533">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2d48c-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d48c-534">Az.Profile</span></span>
* <span data-ttu-id="2d48c-535">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="2d48c-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2d48c-536">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="2d48c-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-537">Az.Compute</span></span>
* <span data-ttu-id="2d48c-538">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="2d48c-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2d48c-539">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d48c-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d48c-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d48c-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d48c-541">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2d48c-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2d48c-542">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d48c-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2d48c-543">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d48c-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d48c-544">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d48c-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d48c-545">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d48c-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-546">Az.Network</span></span>
* <span data-ttu-id="2d48c-547">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2d48c-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2d48c-548">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d48c-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-549">Az.Resources</span></span>
* <span data-ttu-id="2d48c-550">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="2d48c-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2d48c-551">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="2d48c-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2d48c-552">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2d48c-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d48c-553">Azure.Storage</span></span>
* <span data-ttu-id="2d48c-554">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="2d48c-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2d48c-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d48c-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2d48c-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d48c-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d48c-557">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d48c-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2d48c-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2d48c-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2d48c-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d48c-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d48c-560">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="2d48c-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d48c-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d48c-561">Az.Compute</span></span>
* <span data-ttu-id="2d48c-562">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="2d48c-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2d48c-563">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d48c-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2d48c-564">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="2d48c-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2d48c-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d48c-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2d48c-566">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d48c-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d48c-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d48c-567">Az.Network</span></span>
* <span data-ttu-id="2d48c-568">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="2d48c-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2d48c-569">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d48c-569">new cmdlets added</span></span>
    - <span data-ttu-id="2d48c-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d48c-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d48c-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d48c-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d48c-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d48c-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d48c-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d48c-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d48c-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2d48c-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2d48c-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d48c-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2d48c-576">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="2d48c-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2d48c-577">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2d48c-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2d48c-578">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2d48c-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d48c-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d48c-579">Az.RedisCache</span></span>
* <span data-ttu-id="2d48c-580">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="2d48c-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2d48c-581">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2d48c-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d48c-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d48c-582">Az.Resources</span></span>
* <span data-ttu-id="2d48c-583">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d48c-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d48c-584">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="2d48c-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d48c-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d48c-585">Az.Sql</span></span>
* <span data-ttu-id="2d48c-586">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d48c-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d48c-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d48c-587">Az.Websites</span></span>
* <span data-ttu-id="2d48c-588">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="2d48c-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2d48c-589">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="2d48c-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2d48c-590">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="2d48c-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2d48c-591">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="2d48c-591">Initial Release</span></span>