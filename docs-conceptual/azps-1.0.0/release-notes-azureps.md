## <a name="100---december-2018"></a><span data-ttu-id="81036-101">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="81036-102">Ogólne</span><span class="sxs-lookup"><span data-stu-id="81036-102">General</span></span>

- <span data-ttu-id="81036-103">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="81036-103">General Availability of Az Module</span></span>
- <span data-ttu-id="81036-104">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="81036-104">Online help for each module</span></span>
- <span data-ttu-id="81036-105">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="81036-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="81036-106">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="81036-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="81036-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="81036-107">Az.Accounts</span></span>
- <span data-ttu-id="81036-108">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="81036-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="81036-109">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="81036-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="81036-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="81036-110">Az.ApiManagement</span></span>
- <span data-ttu-id="81036-111">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="81036-111">Fixes for #7002</span></span>
- <span data-ttu-id="81036-112">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="81036-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="81036-113">Az.Batch</span></span>
- <span data-ttu-id="81036-114">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="81036-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="81036-115">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="81036-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="81036-116">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="81036-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="81036-117">Az.Billing</span></span>
- <span data-ttu-id="81036-118">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="81036-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="81036-119">Az.CognitivServices</span></span>
- <span data-ttu-id="81036-120">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="81036-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="81036-121">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="81036-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="81036-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="81036-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="81036-123">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="81036-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="81036-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="81036-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="81036-125">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="81036-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81036-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="81036-127">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="81036-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="81036-128">Az.Monitor</span></span>
- <span data-ttu-id="81036-129">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="81036-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81036-130">Az.KeyVault</span></span>
- <span data-ttu-id="81036-131">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="81036-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="81036-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="81036-132">Az.MachineLearning</span></span>
- <span data-ttu-id="81036-133">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="81036-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="81036-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="81036-134">Az.Media</span></span>
- <span data-ttu-id="81036-135">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="81036-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="81036-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="81036-136">Az.Network</span></span>
<span data-ttu-id="81036-137">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="81036-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="81036-138">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="81036-138">New cmdlets added:</span></span>
        - <span data-ttu-id="81036-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="81036-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="81036-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="81036-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="81036-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="81036-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="81036-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="81036-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="81036-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="81036-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="81036-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="81036-147">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81036-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="81036-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81036-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="81036-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81036-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="81036-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81036-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="81036-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81036-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="81036-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81036-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="81036-153">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="81036-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="81036-154">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="81036-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="81036-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81036-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="81036-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81036-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="81036-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81036-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="81036-158">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="81036-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="81036-159">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="81036-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="81036-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="81036-161">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="81036-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="81036-162">Az.Profile</span></span>
- <span data-ttu-id="81036-163">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="81036-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="81036-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="81036-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="81036-165">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="81036-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-166">Az.Resources</span></span>
- <span data-ttu-id="81036-167">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="81036-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81036-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="81036-169">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="81036-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="81036-170">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="81036-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="81036-171">Az.SIgnalR</span></span>
- <span data-ttu-id="81036-172">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="81036-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="81036-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="81036-173">Az.Sql</span></span>
- <span data-ttu-id="81036-174">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="81036-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="81036-175">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="81036-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="81036-176">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="81036-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="81036-177">Az.Storage</span></span>
- <span data-ttu-id="81036-178">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="81036-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="81036-179">Az.Websites</span></span>
- <span data-ttu-id="81036-180">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="81036-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="81036-181">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="81036-182">Ogólne</span><span class="sxs-lookup"><span data-stu-id="81036-182">General</span></span>

* <span data-ttu-id="81036-183">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="81036-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="81036-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="81036-184">Az.Compute</span></span>

* <span data-ttu-id="81036-185">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="81036-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="81036-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81036-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="81036-187">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="81036-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="81036-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="81036-188">Az.FrontDoor</span></span>

* <span data-ttu-id="81036-189">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="81036-189">Fixed some broken links</span></span>
    - <span data-ttu-id="81036-190">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="81036-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="81036-191">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="81036-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="81036-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="81036-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="81036-193">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="81036-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="81036-194">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="81036-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="81036-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-195">Az.Resources</span></span>

* <span data-ttu-id="81036-196">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="81036-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="81036-197">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="81036-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="81036-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="81036-198">Az.Sql</span></span>

* <span data-ttu-id="81036-199">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="81036-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="81036-200">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="81036-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="81036-201">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="81036-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="81036-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="81036-202">Az.Storage</span></span>

* <span data-ttu-id="81036-203">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81036-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="81036-204">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="81036-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="81036-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="81036-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="81036-206">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="81036-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="81036-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="81036-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="81036-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="81036-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="81036-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="81036-209">Az.Websites</span></span>

* <span data-ttu-id="81036-210">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="81036-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="81036-211">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="81036-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="81036-212">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="81036-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="81036-213">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="81036-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="81036-214">Az.ApiManagement</span></span>
* <span data-ttu-id="81036-215">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="81036-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="81036-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="81036-216">Az.Automation</span></span>
* <span data-ttu-id="81036-217">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="81036-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="81036-218">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="81036-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="81036-219">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="81036-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="81036-220">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="81036-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="81036-221">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="81036-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="81036-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="81036-222">Az.Compute</span></span>
* <span data-ttu-id="81036-223">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="81036-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="81036-224">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="81036-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="81036-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="81036-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="81036-226">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="81036-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="81036-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="81036-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="81036-228">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="81036-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="81036-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="81036-229">Az.Network</span></span>
* <span data-ttu-id="81036-230">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="81036-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="81036-231">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="81036-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="81036-232">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="81036-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="81036-233">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81036-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="81036-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="81036-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="81036-235">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="81036-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="81036-236">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="81036-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="81036-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="81036-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="81036-238">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="81036-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="81036-239">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="81036-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="81036-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="81036-240">Az.Relay</span></span>
* <span data-ttu-id="81036-241">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="81036-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="81036-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-242">Az.Resources</span></span>
* <span data-ttu-id="81036-243">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="81036-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="81036-244">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="81036-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="81036-245">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="81036-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="81036-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81036-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="81036-247">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="81036-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="81036-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="81036-248">Az.Sql</span></span>
* <span data-ttu-id="81036-249">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="81036-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="81036-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="81036-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="81036-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="81036-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="81036-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="81036-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="81036-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="81036-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="81036-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="81036-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="81036-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="81036-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="81036-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="81036-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="81036-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="81036-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="81036-258">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="81036-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="81036-259">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="81036-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="81036-260">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="81036-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="81036-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="81036-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="81036-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="81036-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="81036-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="81036-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="81036-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="81036-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="81036-265">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81036-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="81036-266">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="81036-267">Ogólne</span><span class="sxs-lookup"><span data-stu-id="81036-267">General</span></span>
* <span data-ttu-id="81036-268">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="81036-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="81036-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="81036-269">Az.Profile</span></span>
* <span data-ttu-id="81036-270">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="81036-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="81036-271">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="81036-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="81036-272">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="81036-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="81036-273">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="81036-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="81036-274">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="81036-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="81036-275">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="81036-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="81036-276">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="81036-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="81036-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="81036-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="81036-278">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="81036-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="81036-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="81036-279">Az.Compute</span></span>
* <span data-ttu-id="81036-280">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="81036-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="81036-281">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="81036-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="81036-282">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="81036-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="81036-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81036-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="81036-284">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="81036-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="81036-285">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="81036-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="81036-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="81036-286">Az.Insights</span></span>
* <span data-ttu-id="81036-287">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="81036-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="81036-288">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="81036-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="81036-289">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="81036-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="81036-290">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="81036-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="81036-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="81036-291">Az.Network</span></span>
* <span data-ttu-id="81036-292">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="81036-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="81036-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="81036-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="81036-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="81036-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="81036-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="81036-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="81036-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="81036-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="81036-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="81036-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="81036-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="81036-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="81036-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="81036-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="81036-300">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="81036-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="81036-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-301">Az.Resources</span></span>
* <span data-ttu-id="81036-302">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="81036-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="81036-303">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="81036-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="81036-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81036-304">Az.ServiceBus</span></span>
* <span data-ttu-id="81036-305">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="81036-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="81036-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81036-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="81036-307">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="81036-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="81036-308">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="81036-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="81036-309">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="81036-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="81036-310">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="81036-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="81036-311">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="81036-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="81036-312">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="81036-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="81036-313">Az.Profile</span></span>
* <span data-ttu-id="81036-314">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="81036-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="81036-315">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="81036-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="81036-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="81036-316">Az.Compute</span></span>
* <span data-ttu-id="81036-317">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="81036-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="81036-318">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81036-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="81036-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81036-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="81036-320">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="81036-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="81036-321">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81036-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="81036-322">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81036-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="81036-323">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81036-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="81036-324">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81036-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="81036-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="81036-325">Az.Network</span></span>
* <span data-ttu-id="81036-326">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="81036-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="81036-327">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81036-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="81036-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-328">Az.Resources</span></span>
* <span data-ttu-id="81036-329">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="81036-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="81036-330">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="81036-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="81036-331">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="81036-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="81036-332">Azure.Storage</span></span>
* <span data-ttu-id="81036-333">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="81036-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="81036-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="81036-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="81036-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="81036-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="81036-336">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="81036-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="81036-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="81036-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="81036-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="81036-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="81036-339">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="81036-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="81036-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="81036-340">Az.Compute</span></span>
* <span data-ttu-id="81036-341">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="81036-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="81036-342">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="81036-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="81036-343">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="81036-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="81036-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81036-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="81036-345">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="81036-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="81036-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="81036-346">Az.Network</span></span>
* <span data-ttu-id="81036-347">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="81036-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="81036-348">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="81036-348">new cmdlets added</span></span>
    - <span data-ttu-id="81036-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="81036-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="81036-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="81036-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="81036-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="81036-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="81036-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="81036-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="81036-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="81036-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="81036-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="81036-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="81036-355">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="81036-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="81036-356">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="81036-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="81036-357">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="81036-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="81036-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="81036-358">Az.RedisCache</span></span>
* <span data-ttu-id="81036-359">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="81036-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="81036-360">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="81036-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="81036-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="81036-361">Az.Resources</span></span>
* <span data-ttu-id="81036-362">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="81036-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="81036-363">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="81036-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="81036-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="81036-364">Az.Sql</span></span>
* <span data-ttu-id="81036-365">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="81036-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="81036-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="81036-366">Az.Websites</span></span>
* <span data-ttu-id="81036-367">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="81036-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="81036-368">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="81036-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="81036-369">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="81036-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="81036-370">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="81036-370">Initial Release</span></span>