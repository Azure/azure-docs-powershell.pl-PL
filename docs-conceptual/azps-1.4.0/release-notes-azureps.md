## <a name="140---february-2019"></a><span data-ttu-id="a6cf7-101">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a6cf7-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6cf7-103">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="a6cf7-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6cf7-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6cf7-104">Az.Automation</span></span>
* <span data-ttu-id="a6cf7-105">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a6cf7-106">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a6cf7-107">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6cf7-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6cf7-109">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-110">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-111">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a6cf7-112">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="a6cf7-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a6cf7-113">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a6cf7-114">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6cf7-116">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="a6cf7-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6cf7-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6cf7-117">Az.EventHub</span></span>
* <span data-ttu-id="a6cf7-118">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="a6cf7-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a6cf7-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6cf7-119">Az.KeyVault</span></span>
* <span data-ttu-id="a6cf7-120">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6cf7-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6cf7-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6cf7-121">Az.LogicApp</span></span>
* <span data-ttu-id="a6cf7-122">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="a6cf7-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a6cf7-123">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="a6cf7-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a6cf7-124">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="a6cf7-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a6cf7-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6cf7-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6cf7-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6cf7-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6cf7-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6cf7-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6cf7-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6cf7-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a6cf7-129">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="a6cf7-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a6cf7-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6cf7-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6cf7-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6cf7-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a6cf7-134">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a6cf7-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6cf7-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6cf7-135">Az.Monitor</span></span>
* <span data-ttu-id="a6cf7-136">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a6cf7-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6cf7-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-137">Az.Network</span></span>
* <span data-ttu-id="a6cf7-138">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a6cf7-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6cf7-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6cf7-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6cf7-140">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a6cf7-141">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a6cf7-142">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a6cf7-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-143">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-144">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a6cf7-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6cf7-145">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a6cf7-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a6cf7-146">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a6cf7-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a6cf7-147">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a6cf7-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6cf7-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-148">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-149">Dodano obsługę warstwy bazy danych SQL w hiperskali</span><span class="sxs-lookup"><span data-stu-id="a6cf7-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a6cf7-150">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="a6cf7-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6cf7-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-151">Az.Websites</span></span>
* <span data-ttu-id="a6cf7-152">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a6cf7-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a6cf7-153">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6cf7-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-154">Az.Accounts</span></span>
* <span data-ttu-id="a6cf7-155">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6cf7-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6cf7-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-156">Az.AnalysisServices</span></span>
<span data-ttu-id="a6cf7-157">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-158">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-159">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="a6cf7-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a6cf7-160">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a6cf7-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a6cf7-161">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6cf7-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-162">Az.RecoveryServices</span></span>
<span data-ttu-id="a6cf7-163">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-164">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-165">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a6cf7-166">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a6cf7-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6cf7-167">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a6cf7-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a6cf7-168">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a6cf7-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6cf7-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-169">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-170">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a6cf7-171">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="a6cf7-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a6cf7-172">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a6cf7-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a6cf7-173">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6cf7-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-174">Az.Accounts</span></span>
* <span data-ttu-id="a6cf7-175">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a6cf7-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6cf7-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6cf7-177">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a6cf7-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6cf7-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6cf7-179">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a6cf7-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a6cf7-180">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6cf7-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-181">Az.Accounts</span></span>
* <span data-ttu-id="a6cf7-182">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a6cf7-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6cf7-183">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6cf7-184">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a6cf7-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6cf7-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6cf7-185">Az.Aks</span></span>
* <span data-ttu-id="a6cf7-186">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6cf7-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6cf7-187">Az.Automation</span></span>
* <span data-ttu-id="a6cf7-188">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="a6cf7-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a6cf7-189">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6cf7-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6cf7-190">Az.Cdn</span></span>
* <span data-ttu-id="a6cf7-191">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-192">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-193">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a6cf7-194">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6cf7-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a6cf7-195">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6cf7-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a6cf7-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a6cf7-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a6cf7-197">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6cf7-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6cf7-198">Az.DataFactory</span></span>
* <span data-ttu-id="a6cf7-199">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a6cf7-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6cf7-201">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="a6cf7-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a6cf7-202">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a6cf7-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a6cf7-203">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6cf7-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6cf7-204">Az.IotHub</span></span>
* <span data-ttu-id="a6cf7-205">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6cf7-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6cf7-206">Az.KeyVault</span></span>
* <span data-ttu-id="a6cf7-207">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6cf7-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-208">Az.Network</span></span>
* <span data-ttu-id="a6cf7-209">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-210">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-211">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a6cf7-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a6cf7-212">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a6cf7-213">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cf7-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a6cf7-214">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a6cf7-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a6cf7-215">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a6cf7-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a6cf7-216">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a6cf7-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a6cf7-217">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a6cf7-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6cf7-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6cf7-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6cf7-219">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a6cf7-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a6cf7-220">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-220">Fix some error messages.</span></span>
* <span data-ttu-id="a6cf7-221">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a6cf7-222">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6cf7-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6cf7-223">Az.SignalR</span></span>
* <span data-ttu-id="a6cf7-224">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6cf7-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-225">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-226">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6cf7-227">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="a6cf7-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a6cf7-228">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="a6cf7-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a6cf7-229">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="a6cf7-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6cf7-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-230">Az.Storage</span></span>
* <span data-ttu-id="a6cf7-231">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6cf7-232">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a6cf7-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a6cf7-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a6cf7-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a6cf7-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a6cf7-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a6cf7-235">Az.TrafficManager</span></span>
* <span data-ttu-id="a6cf7-236">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6cf7-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-237">Az.Websites</span></span>
* <span data-ttu-id="a6cf7-238">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a6cf7-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6cf7-239">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a6cf7-240">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="a6cf7-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a6cf7-241">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6cf7-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-242">Az.Accounts</span></span>
* <span data-ttu-id="a6cf7-243">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a6cf7-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-244">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-245">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a6cf7-246">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a6cf7-247">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6cf7-249">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a6cf7-250">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="a6cf7-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6cf7-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6cf7-251">Az.EventGrid</span></span>
* <span data-ttu-id="a6cf7-252">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a6cf7-253">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a6cf7-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a6cf7-254">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="a6cf7-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6cf7-255">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="a6cf7-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6cf7-256">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="a6cf7-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6cf7-257">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a6cf7-258">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="a6cf7-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6cf7-259">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="a6cf7-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6cf7-260">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="a6cf7-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6cf7-261">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="a6cf7-262">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a6cf7-263">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6cf7-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6cf7-264">Az.IotHub</span></span>
* <span data-ttu-id="a6cf7-265">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="a6cf7-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6cf7-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6cf7-266">Az.LogicApp</span></span>
* <span data-ttu-id="a6cf7-267">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-268">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-269">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a6cf7-270">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a6cf7-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a6cf7-271">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cf7-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6cf7-272">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a6cf7-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a6cf7-273">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a6cf7-274">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a6cf7-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6cf7-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6cf7-275">Az.SignalR</span></span>
* <span data-ttu-id="a6cf7-276">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6cf7-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-277">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-278">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6cf7-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-279">Az.Storage</span></span>
* <span data-ttu-id="a6cf7-280">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="a6cf7-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a6cf7-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6cf7-281">New-AzStorageContext</span></span>
* <span data-ttu-id="a6cf7-282">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="a6cf7-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a6cf7-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6cf7-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6cf7-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-284">Az.Websites</span></span>
* <span data-ttu-id="a6cf7-285">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a6cf7-286">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a6cf7-287">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a6cf7-288">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a6cf7-288">General</span></span>

- <span data-ttu-id="a6cf7-289">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="a6cf7-289">General Availability of Az Module</span></span>
- <span data-ttu-id="a6cf7-290">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="a6cf7-290">Online help for each module</span></span>
- <span data-ttu-id="a6cf7-291">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a6cf7-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a6cf7-292">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="a6cf7-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a6cf7-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-293">Az.Accounts</span></span>
- <span data-ttu-id="a6cf7-294">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="a6cf7-295">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="a6cf7-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6cf7-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6cf7-296">Az.ApiManagement</span></span>
- <span data-ttu-id="a6cf7-297">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="a6cf7-297">Fixes for #7002</span></span>
- <span data-ttu-id="a6cf7-298">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a6cf7-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6cf7-299">Az.Batch</span></span>
- <span data-ttu-id="a6cf7-300">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a6cf7-301">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a6cf7-302">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a6cf7-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a6cf7-303">Az.Billing</span></span>
- <span data-ttu-id="a6cf7-304">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a6cf7-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-305">Az.CognitivServices</span></span>
- <span data-ttu-id="a6cf7-306">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a6cf7-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a6cf7-307">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a6cf7-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6cf7-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="a6cf7-309">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a6cf7-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a6cf7-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a6cf7-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a6cf7-311">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="a6cf7-313">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a6cf7-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6cf7-314">Az.Monitor</span></span>
- <span data-ttu-id="a6cf7-315">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a6cf7-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6cf7-316">Az.KeyVault</span></span>
- <span data-ttu-id="a6cf7-317">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="a6cf7-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a6cf7-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6cf7-318">Az.MachineLearning</span></span>
- <span data-ttu-id="a6cf7-319">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a6cf7-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a6cf7-320">Az.Media</span></span>
- <span data-ttu-id="a6cf7-321">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a6cf7-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6cf7-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-322">Az.Network</span></span>
<span data-ttu-id="a6cf7-323">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a6cf7-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a6cf7-324">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6cf7-324">New cmdlets added:</span></span>
        - <span data-ttu-id="a6cf7-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a6cf7-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a6cf7-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a6cf7-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6cf7-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a6cf7-333">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a6cf7-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6cf7-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a6cf7-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6cf7-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6cf7-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6cf7-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6cf7-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6cf7-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a6cf7-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a6cf7-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a6cf7-339">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a6cf7-340">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6cf7-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a6cf7-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6cf7-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6cf7-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6cf7-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6cf7-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6cf7-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a6cf7-344">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a6cf7-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a6cf7-345">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a6cf7-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6cf7-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="a6cf7-347">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a6cf7-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-348">Az.Profile</span></span>
- <span data-ttu-id="a6cf7-349">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6cf7-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6cf7-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="a6cf7-351">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a6cf7-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-352">Az.Resources</span></span>
- <span data-ttu-id="a6cf7-353">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6cf7-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6cf7-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="a6cf7-355">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="a6cf7-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a6cf7-356">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a6cf7-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6cf7-357">Az.SIgnalR</span></span>
- <span data-ttu-id="a6cf7-358">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6cf7-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a6cf7-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-359">Az.Sql</span></span>
- <span data-ttu-id="a6cf7-360">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="a6cf7-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a6cf7-361">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a6cf7-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a6cf7-362">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6cf7-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-363">Az.Storage</span></span>
- <span data-ttu-id="a6cf7-364">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6cf7-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-365">Az.Websites</span></span>
- <span data-ttu-id="a6cf7-366">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6cf7-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a6cf7-367">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a6cf7-368">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a6cf7-368">General</span></span>

* <span data-ttu-id="a6cf7-369">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="a6cf7-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6cf7-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-370">Az.Compute</span></span>

* <span data-ttu-id="a6cf7-371">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="a6cf7-373">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="a6cf7-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a6cf7-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6cf7-374">Az.FrontDoor</span></span>

* <span data-ttu-id="a6cf7-375">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="a6cf7-375">Fixed some broken links</span></span>
    - <span data-ttu-id="a6cf7-376">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a6cf7-377">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6cf7-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="a6cf7-379">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a6cf7-380">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6cf7-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-381">Az.Resources</span></span>

* <span data-ttu-id="a6cf7-382">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a6cf7-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a6cf7-383">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a6cf7-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-384">Az.Sql</span></span>

* <span data-ttu-id="a6cf7-385">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="a6cf7-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a6cf7-386">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="a6cf7-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a6cf7-387">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6cf7-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-388">Az.Storage</span></span>

* <span data-ttu-id="a6cf7-389">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6cf7-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a6cf7-390">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="a6cf7-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a6cf7-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6cf7-392">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="a6cf7-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="a6cf7-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6cf7-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a6cf7-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6cf7-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6cf7-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-395">Az.Websites</span></span>

* <span data-ttu-id="a6cf7-396">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a6cf7-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a6cf7-397">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a6cf7-398">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a6cf7-399">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6cf7-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6cf7-400">Az.ApiManagement</span></span>
* <span data-ttu-id="a6cf7-401">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a6cf7-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6cf7-402">Az.Automation</span></span>
* <span data-ttu-id="a6cf7-403">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="a6cf7-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a6cf7-404">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="a6cf7-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a6cf7-405">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="a6cf7-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a6cf7-406">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a6cf7-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a6cf7-407">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="a6cf7-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6cf7-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-408">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-409">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a6cf7-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a6cf7-410">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6cf7-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6cf7-412">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a6cf7-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a6cf7-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a6cf7-414">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="a6cf7-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6cf7-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-415">Az.Network</span></span>
* <span data-ttu-id="a6cf7-416">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a6cf7-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a6cf7-417">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a6cf7-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a6cf7-418">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a6cf7-419">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a6cf7-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a6cf7-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a6cf7-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a6cf7-421">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a6cf7-422">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a6cf7-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a6cf7-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a6cf7-424">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a6cf7-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a6cf7-425">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a6cf7-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a6cf7-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a6cf7-426">Az.Relay</span></span>
* <span data-ttu-id="a6cf7-427">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6cf7-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-428">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-429">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a6cf7-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a6cf7-430">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="a6cf7-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a6cf7-431">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a6cf7-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6cf7-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6cf7-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6cf7-433">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="a6cf7-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a6cf7-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-434">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-435">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a6cf7-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a6cf7-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6cf7-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6cf7-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6cf7-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6cf7-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6cf7-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6cf7-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6cf7-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6cf7-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6cf7-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6cf7-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6cf7-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6cf7-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a6cf7-444">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a6cf7-445">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a6cf7-446">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a6cf7-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6cf7-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6cf7-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a6cf7-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a6cf7-451">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a6cf7-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a6cf7-452">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a6cf7-453">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a6cf7-453">General</span></span>
* <span data-ttu-id="a6cf7-454">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a6cf7-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-455">Az.Profile</span></span>
* <span data-ttu-id="a6cf7-456">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="a6cf7-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a6cf7-457">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="a6cf7-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a6cf7-458">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a6cf7-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a6cf7-459">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a6cf7-460">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="a6cf7-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a6cf7-461">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="a6cf7-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a6cf7-462">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="a6cf7-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6cf7-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6cf7-464">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-465">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-466">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a6cf7-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a6cf7-467">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a6cf7-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a6cf7-468">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6cf7-470">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a6cf7-471">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a6cf7-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a6cf7-472">Az.Insights</span></span>
* <span data-ttu-id="a6cf7-473">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="a6cf7-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a6cf7-474">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="a6cf7-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a6cf7-475">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="a6cf7-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a6cf7-476">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a6cf7-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6cf7-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-477">Az.Network</span></span>
* <span data-ttu-id="a6cf7-478">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6cf7-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a6cf7-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6cf7-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a6cf7-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a6cf7-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a6cf7-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6cf7-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a6cf7-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a6cf7-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a6cf7-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6cf7-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a6cf7-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6cf7-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6cf7-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6cf7-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6cf7-486">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="a6cf7-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-487">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-488">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a6cf7-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a6cf7-489">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6cf7-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6cf7-490">Az.ServiceBus</span></span>
* <span data-ttu-id="a6cf7-491">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6cf7-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6cf7-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6cf7-493">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a6cf7-494">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a6cf7-495">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a6cf7-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a6cf7-496">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a6cf7-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a6cf7-497">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a6cf7-498">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a6cf7-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-499">Az.Profile</span></span>
* <span data-ttu-id="a6cf7-500">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="a6cf7-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a6cf7-501">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="a6cf7-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-502">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-503">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="a6cf7-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a6cf7-504">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6cf7-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6cf7-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6cf7-506">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a6cf7-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a6cf7-507">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a6cf7-508">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6cf7-509">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6cf7-510">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6cf7-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-511">Az.Network</span></span>
* <span data-ttu-id="a6cf7-512">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a6cf7-513">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-514">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-515">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a6cf7-516">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a6cf7-517">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a6cf7-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-518">Azure.Storage</span></span>
* <span data-ttu-id="a6cf7-519">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="a6cf7-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a6cf7-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a6cf7-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6cf7-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6cf7-522">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a6cf7-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a6cf7-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a6cf7-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6cf7-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6cf7-525">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6cf7-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6cf7-526">Az.Compute</span></span>
* <span data-ttu-id="a6cf7-527">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="a6cf7-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a6cf7-528">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a6cf7-529">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="a6cf7-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a6cf7-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a6cf7-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a6cf7-531">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6cf7-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6cf7-532">Az.Network</span></span>
* <span data-ttu-id="a6cf7-533">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a6cf7-534">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6cf7-534">new cmdlets added</span></span>
    - <span data-ttu-id="a6cf7-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6cf7-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6cf7-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6cf7-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6cf7-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6cf7-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a6cf7-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a6cf7-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6cf7-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a6cf7-541">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="a6cf7-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a6cf7-542">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a6cf7-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a6cf7-543">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a6cf7-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6cf7-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6cf7-544">Az.RedisCache</span></span>
* <span data-ttu-id="a6cf7-545">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a6cf7-546">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a6cf7-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6cf7-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6cf7-547">Az.Resources</span></span>
* <span data-ttu-id="a6cf7-548">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cf7-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6cf7-549">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="a6cf7-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6cf7-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6cf7-550">Az.Sql</span></span>
* <span data-ttu-id="a6cf7-551">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a6cf7-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6cf7-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6cf7-552">Az.Websites</span></span>
* <span data-ttu-id="a6cf7-553">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="a6cf7-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a6cf7-554">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="a6cf7-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a6cf7-555">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a6cf7-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a6cf7-556">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="a6cf7-556">Initial Release</span></span>