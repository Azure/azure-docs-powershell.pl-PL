---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342151"
---
## <a name="110---january-2019"></a><span data-ttu-id="73d1a-101">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73d1a-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-102">Az.Accounts</span></span>
* <span data-ttu-id="73d1a-103">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="73d1a-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73d1a-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-104">Az.Compute</span></span>
* <span data-ttu-id="73d1a-105">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="73d1a-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="73d1a-106">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="73d1a-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="73d1a-107">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73d1a-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73d1a-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="73d1a-109">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="73d1a-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="73d1a-110">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="73d1a-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73d1a-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73d1a-111">Az.EventGrid</span></span>
* <span data-ttu-id="73d1a-112">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="73d1a-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="73d1a-113">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="73d1a-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="73d1a-114">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="73d1a-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73d1a-115">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="73d1a-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73d1a-116">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="73d1a-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73d1a-117">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="73d1a-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="73d1a-118">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="73d1a-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73d1a-119">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="73d1a-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73d1a-120">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="73d1a-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73d1a-121">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="73d1a-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="73d1a-122">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="73d1a-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="73d1a-123">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73d1a-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73d1a-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73d1a-124">Az.IotHub</span></span>
* <span data-ttu-id="73d1a-125">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="73d1a-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73d1a-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73d1a-126">Az.LogicApp</span></span>
* <span data-ttu-id="73d1a-127">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="73d1a-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="73d1a-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-128">Az.Resources</span></span>
* <span data-ttu-id="73d1a-129">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="73d1a-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="73d1a-130">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="73d1a-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="73d1a-131">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="73d1a-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73d1a-132">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="73d1a-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="73d1a-133">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="73d1a-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="73d1a-134">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="73d1a-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73d1a-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73d1a-135">Az.SignalR</span></span>
* <span data-ttu-id="73d1a-136">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="73d1a-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73d1a-137">Az.Sql</span></span>
* <span data-ttu-id="73d1a-138">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="73d1a-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73d1a-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73d1a-139">Az.Storage</span></span>
* <span data-ttu-id="73d1a-140">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="73d1a-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="73d1a-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73d1a-141">New-AzStorageContext</span></span>
* <span data-ttu-id="73d1a-142">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="73d1a-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="73d1a-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73d1a-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73d1a-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73d1a-144">Az.Websites</span></span>
* <span data-ttu-id="73d1a-145">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="73d1a-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73d1a-146">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="73d1a-147">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="73d1a-148">Ogólne</span><span class="sxs-lookup"><span data-stu-id="73d1a-148">General</span></span>

- <span data-ttu-id="73d1a-149">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="73d1a-149">General Availability of Az Module</span></span>
- <span data-ttu-id="73d1a-150">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="73d1a-150">Online help for each module</span></span>
- <span data-ttu-id="73d1a-151">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="73d1a-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="73d1a-152">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="73d1a-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="73d1a-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-153">Az.Accounts</span></span>
- <span data-ttu-id="73d1a-154">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73d1a-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="73d1a-155">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="73d1a-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73d1a-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73d1a-156">Az.ApiManagement</span></span>
- <span data-ttu-id="73d1a-157">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="73d1a-157">Fixes for #7002</span></span>
- <span data-ttu-id="73d1a-158">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="73d1a-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73d1a-159">Az.Batch</span></span>
- <span data-ttu-id="73d1a-160">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="73d1a-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="73d1a-161">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="73d1a-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="73d1a-162">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="73d1a-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73d1a-163">Az.Billing</span></span>
- <span data-ttu-id="73d1a-164">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="73d1a-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="73d1a-165">Az.CognitivServices</span></span>
- <span data-ttu-id="73d1a-166">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="73d1a-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="73d1a-167">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="73d1a-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73d1a-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="73d1a-169">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="73d1a-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="73d1a-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="73d1a-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="73d1a-171">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73d1a-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73d1a-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="73d1a-173">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="73d1a-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73d1a-174">Az.Monitor</span></span>
- <span data-ttu-id="73d1a-175">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="73d1a-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73d1a-176">Az.KeyVault</span></span>
- <span data-ttu-id="73d1a-177">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="73d1a-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="73d1a-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73d1a-178">Az.MachineLearning</span></span>
- <span data-ttu-id="73d1a-179">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="73d1a-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="73d1a-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73d1a-180">Az.Media</span></span>
- <span data-ttu-id="73d1a-181">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="73d1a-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73d1a-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73d1a-182">Az.Network</span></span>
<span data-ttu-id="73d1a-183">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="73d1a-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="73d1a-184">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73d1a-184">New cmdlets added:</span></span>
        - <span data-ttu-id="73d1a-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="73d1a-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="73d1a-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="73d1a-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="73d1a-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="73d1a-193">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73d1a-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="73d1a-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73d1a-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="73d1a-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73d1a-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73d1a-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73d1a-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73d1a-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73d1a-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="73d1a-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73d1a-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="73d1a-199">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="73d1a-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="73d1a-200">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="73d1a-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="73d1a-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73d1a-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73d1a-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73d1a-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73d1a-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73d1a-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="73d1a-204">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="73d1a-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="73d1a-205">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="73d1a-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73d1a-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="73d1a-207">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="73d1a-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73d1a-208">Az.Profile</span></span>
- <span data-ttu-id="73d1a-209">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73d1a-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73d1a-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73d1a-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="73d1a-211">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="73d1a-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-212">Az.Resources</span></span>
- <span data-ttu-id="73d1a-213">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73d1a-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73d1a-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="73d1a-215">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="73d1a-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="73d1a-216">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="73d1a-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73d1a-217">Az.SIgnalR</span></span>
- <span data-ttu-id="73d1a-218">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73d1a-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="73d1a-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73d1a-219">Az.Sql</span></span>
- <span data-ttu-id="73d1a-220">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="73d1a-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="73d1a-221">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="73d1a-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="73d1a-222">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="73d1a-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73d1a-223">Az.Storage</span></span>
- <span data-ttu-id="73d1a-224">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73d1a-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73d1a-225">Az.Websites</span></span>
- <span data-ttu-id="73d1a-226">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="73d1a-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="73d1a-227">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="73d1a-228">Ogólne</span><span class="sxs-lookup"><span data-stu-id="73d1a-228">General</span></span>

* <span data-ttu-id="73d1a-229">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="73d1a-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="73d1a-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-230">Az.Compute</span></span>

* <span data-ttu-id="73d1a-231">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="73d1a-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73d1a-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73d1a-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="73d1a-233">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="73d1a-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="73d1a-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73d1a-234">Az.FrontDoor</span></span>

* <span data-ttu-id="73d1a-235">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="73d1a-235">Fixed some broken links</span></span>
    - <span data-ttu-id="73d1a-236">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="73d1a-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="73d1a-237">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="73d1a-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73d1a-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73d1a-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="73d1a-239">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73d1a-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="73d1a-240">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73d1a-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="73d1a-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-241">Az.Resources</span></span>

* <span data-ttu-id="73d1a-242">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="73d1a-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="73d1a-243">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="73d1a-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="73d1a-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73d1a-244">Az.Sql</span></span>

* <span data-ttu-id="73d1a-245">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="73d1a-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="73d1a-246">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="73d1a-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="73d1a-247">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="73d1a-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="73d1a-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73d1a-248">Az.Storage</span></span>

* <span data-ttu-id="73d1a-249">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73d1a-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="73d1a-250">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="73d1a-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="73d1a-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73d1a-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73d1a-252">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="73d1a-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="73d1a-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73d1a-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="73d1a-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73d1a-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73d1a-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73d1a-255">Az.Websites</span></span>

* <span data-ttu-id="73d1a-256">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73d1a-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="73d1a-257">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="73d1a-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="73d1a-258">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="73d1a-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="73d1a-259">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73d1a-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73d1a-260">Az.ApiManagement</span></span>
* <span data-ttu-id="73d1a-261">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="73d1a-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="73d1a-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73d1a-262">Az.Automation</span></span>
* <span data-ttu-id="73d1a-263">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="73d1a-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="73d1a-264">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="73d1a-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="73d1a-265">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="73d1a-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="73d1a-266">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="73d1a-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="73d1a-267">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="73d1a-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="73d1a-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-268">Az.Compute</span></span>
* <span data-ttu-id="73d1a-269">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="73d1a-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="73d1a-270">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="73d1a-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73d1a-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="73d1a-272">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="73d1a-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="73d1a-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73d1a-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73d1a-274">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="73d1a-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73d1a-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73d1a-275">Az.Network</span></span>
* <span data-ttu-id="73d1a-276">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="73d1a-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="73d1a-277">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="73d1a-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="73d1a-278">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="73d1a-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="73d1a-279">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73d1a-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="73d1a-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="73d1a-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="73d1a-281">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="73d1a-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="73d1a-282">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="73d1a-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="73d1a-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="73d1a-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="73d1a-284">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73d1a-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="73d1a-285">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="73d1a-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="73d1a-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73d1a-286">Az.Relay</span></span>
* <span data-ttu-id="73d1a-287">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="73d1a-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="73d1a-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-288">Az.Resources</span></span>
* <span data-ttu-id="73d1a-289">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="73d1a-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="73d1a-290">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="73d1a-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="73d1a-291">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="73d1a-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73d1a-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73d1a-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="73d1a-293">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="73d1a-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="73d1a-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73d1a-294">Az.Sql</span></span>
* <span data-ttu-id="73d1a-295">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="73d1a-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="73d1a-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73d1a-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73d1a-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73d1a-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73d1a-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73d1a-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73d1a-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73d1a-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73d1a-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73d1a-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73d1a-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73d1a-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73d1a-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="73d1a-304">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="73d1a-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="73d1a-305">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="73d1a-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="73d1a-306">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="73d1a-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="73d1a-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73d1a-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73d1a-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73d1a-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73d1a-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73d1a-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="73d1a-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73d1a-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="73d1a-311">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="73d1a-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="73d1a-312">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="73d1a-313">Ogólne</span><span class="sxs-lookup"><span data-stu-id="73d1a-313">General</span></span>
* <span data-ttu-id="73d1a-314">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="73d1a-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="73d1a-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73d1a-315">Az.Profile</span></span>
* <span data-ttu-id="73d1a-316">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="73d1a-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="73d1a-317">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="73d1a-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="73d1a-318">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="73d1a-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="73d1a-319">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="73d1a-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="73d1a-320">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="73d1a-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="73d1a-321">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="73d1a-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="73d1a-322">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="73d1a-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="73d1a-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73d1a-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="73d1a-324">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="73d1a-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73d1a-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-325">Az.Compute</span></span>
* <span data-ttu-id="73d1a-326">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="73d1a-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="73d1a-327">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="73d1a-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="73d1a-328">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="73d1a-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73d1a-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73d1a-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="73d1a-330">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="73d1a-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="73d1a-331">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="73d1a-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="73d1a-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="73d1a-332">Az.Insights</span></span>
* <span data-ttu-id="73d1a-333">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="73d1a-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="73d1a-334">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="73d1a-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="73d1a-335">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="73d1a-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="73d1a-336">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="73d1a-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73d1a-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73d1a-337">Az.Network</span></span>
* <span data-ttu-id="73d1a-338">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73d1a-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="73d1a-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="73d1a-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="73d1a-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="73d1a-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="73d1a-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73d1a-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="73d1a-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="73d1a-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="73d1a-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="73d1a-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="73d1a-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73d1a-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73d1a-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73d1a-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="73d1a-346">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="73d1a-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73d1a-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-347">Az.Resources</span></span>
* <span data-ttu-id="73d1a-348">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="73d1a-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="73d1a-349">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="73d1a-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73d1a-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73d1a-350">Az.ServiceBus</span></span>
* <span data-ttu-id="73d1a-351">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="73d1a-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73d1a-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73d1a-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="73d1a-353">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="73d1a-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="73d1a-354">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="73d1a-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="73d1a-355">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="73d1a-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="73d1a-356">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="73d1a-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="73d1a-357">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="73d1a-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="73d1a-358">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="73d1a-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73d1a-359">Az.Profile</span></span>
* <span data-ttu-id="73d1a-360">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="73d1a-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="73d1a-361">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="73d1a-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73d1a-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-362">Az.Compute</span></span>
* <span data-ttu-id="73d1a-363">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="73d1a-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="73d1a-364">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73d1a-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73d1a-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73d1a-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="73d1a-366">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="73d1a-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="73d1a-367">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73d1a-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="73d1a-368">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73d1a-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73d1a-369">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73d1a-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73d1a-370">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73d1a-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73d1a-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73d1a-371">Az.Network</span></span>
* <span data-ttu-id="73d1a-372">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73d1a-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="73d1a-373">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73d1a-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73d1a-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-374">Az.Resources</span></span>
* <span data-ttu-id="73d1a-375">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="73d1a-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="73d1a-376">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="73d1a-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="73d1a-377">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="73d1a-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="73d1a-378">Azure.Storage</span></span>
* <span data-ttu-id="73d1a-379">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="73d1a-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="73d1a-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73d1a-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="73d1a-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73d1a-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73d1a-382">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="73d1a-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="73d1a-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="73d1a-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="73d1a-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73d1a-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="73d1a-385">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="73d1a-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73d1a-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73d1a-386">Az.Compute</span></span>
* <span data-ttu-id="73d1a-387">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="73d1a-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="73d1a-388">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="73d1a-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="73d1a-389">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="73d1a-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="73d1a-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="73d1a-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="73d1a-391">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="73d1a-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73d1a-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73d1a-392">Az.Network</span></span>
* <span data-ttu-id="73d1a-393">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="73d1a-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="73d1a-394">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="73d1a-394">new cmdlets added</span></span>
    - <span data-ttu-id="73d1a-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73d1a-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="73d1a-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73d1a-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="73d1a-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73d1a-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="73d1a-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73d1a-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="73d1a-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="73d1a-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="73d1a-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="73d1a-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="73d1a-401">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="73d1a-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="73d1a-402">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="73d1a-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="73d1a-403">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="73d1a-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73d1a-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73d1a-404">Az.RedisCache</span></span>
* <span data-ttu-id="73d1a-405">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="73d1a-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="73d1a-406">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="73d1a-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="73d1a-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73d1a-407">Az.Resources</span></span>
* <span data-ttu-id="73d1a-408">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="73d1a-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73d1a-409">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="73d1a-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="73d1a-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73d1a-410">Az.Sql</span></span>
* <span data-ttu-id="73d1a-411">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="73d1a-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73d1a-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73d1a-412">Az.Websites</span></span>
* <span data-ttu-id="73d1a-413">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="73d1a-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="73d1a-414">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="73d1a-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="73d1a-415">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="73d1a-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="73d1a-416">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="73d1a-416">Initial Release</span></span>