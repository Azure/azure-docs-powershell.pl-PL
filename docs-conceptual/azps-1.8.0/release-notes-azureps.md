---
ms.openlocfilehash: ffeba2cff2e157e7ec0fb7639f9d4075c359c85e
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863834"
---
## <a name="180---april-2019"></a><span data-ttu-id="92dd9-101">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="92dd9-102">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="92dd9-102">Highlights since the last major release</span></span>
* <span data-ttu-id="92dd9-103">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="92dd9-103">General availability of `Az` module</span></span>
* <span data-ttu-id="92dd9-104">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="92dd9-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="92dd9-105">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="92dd9-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="92dd9-106">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="92dd9-107">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="92dd9-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="92dd9-108">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="92dd9-109">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="92dd9-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-110">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-111">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="92dd9-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="92dd9-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="92dd9-112">Az.Batch</span></span>
* <span data-ttu-id="92dd9-113">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="92dd9-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="92dd9-114">Az.Cdn</span></span>
* <span data-ttu-id="92dd9-115">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="92dd9-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="92dd9-117">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-118">Az.Compute</span></span>
* <span data-ttu-id="92dd9-119">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="92dd9-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="92dd9-120">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-121">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="92dd9-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="92dd9-122">Az.DataFactory</span></span>
* <span data-ttu-id="92dd9-123">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="92dd9-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-125">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="92dd9-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="92dd9-126">Az.EventGrid</span></span>
* <span data-ttu-id="92dd9-127">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="92dd9-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="92dd9-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-128">Az.EventHub</span></span>
* <span data-ttu-id="92dd9-129">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="92dd9-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="92dd9-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="92dd9-130">Az.HDInsight</span></span>
* <span data-ttu-id="92dd9-131">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="92dd9-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-132">Az.IotHub</span></span>
* <span data-ttu-id="92dd9-133">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="92dd9-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-134">Az.KeyVault</span></span>
* <span data-ttu-id="92dd9-135">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-136">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="92dd9-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="92dd9-137">Az.MachineLearning</span></span>
* <span data-ttu-id="92dd9-138">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="92dd9-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="92dd9-139">Az.Media</span></span>
* <span data-ttu-id="92dd9-140">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="92dd9-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="92dd9-141">Az.Monitor</span></span>
  * <span data-ttu-id="92dd9-142">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="92dd9-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="92dd9-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="92dd9-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="92dd9-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="92dd9-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="92dd9-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="92dd9-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="92dd9-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="92dd9-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="92dd9-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="92dd9-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="92dd9-148">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="92dd9-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-149">Az.Network</span></span>
* <span data-ttu-id="92dd9-150">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-151">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="92dd9-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="92dd9-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="92dd9-153">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="92dd9-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="92dd9-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="92dd9-155">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="92dd9-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="92dd9-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="92dd9-157">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="92dd9-159">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-160">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="92dd9-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="92dd9-161">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="92dd9-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="92dd9-162">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="92dd9-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="92dd9-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="92dd9-163">Az.RedisCache</span></span>
* <span data-ttu-id="92dd9-164">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-165">Az.Resources</span></span>
* <span data-ttu-id="92dd9-166">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-167">Az.Sql</span></span>
* <span data-ttu-id="92dd9-168">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="92dd9-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="92dd9-169">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-170">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="92dd9-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="92dd9-171">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="92dd9-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="92dd9-172">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="92dd9-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="92dd9-173">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="92dd9-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="92dd9-174">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-175">Az.Websites</span></span>
* <span data-ttu-id="92dd9-176">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="92dd9-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="92dd9-177">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="92dd9-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="92dd9-178">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="92dd9-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="92dd9-179">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="92dd9-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="92dd9-180">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="92dd9-181">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="92dd9-181">Highlights since the last major release</span></span>
* <span data-ttu-id="92dd9-182">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="92dd9-182">General availability of `Az` module</span></span>
* <span data-ttu-id="92dd9-183">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="92dd9-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="92dd9-184">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="92dd9-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="92dd9-185">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="92dd9-186">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="92dd9-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="92dd9-187">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="92dd9-188">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="92dd9-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-189">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-190">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="92dd9-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="92dd9-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="92dd9-192">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="92dd9-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="92dd9-193">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="92dd9-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="92dd9-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-194">Az.Automation</span></span>
* <span data-ttu-id="92dd9-195">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="92dd9-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="92dd9-196">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="92dd9-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="92dd9-197">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-198">Az.Compute</span></span>
* <span data-ttu-id="92dd9-199">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="92dd9-200">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="92dd9-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="92dd9-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="92dd9-202">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="92dd9-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="92dd9-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="92dd9-203">Az.DataFactory</span></span>
* <span data-ttu-id="92dd9-204">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="92dd9-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="92dd9-205">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="92dd9-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-206">Az.Resources</span></span>
* <span data-ttu-id="92dd9-207">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="92dd9-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="92dd9-208">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="92dd9-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="92dd9-209">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="92dd9-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="92dd9-210">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="92dd9-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="92dd9-211">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="92dd9-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="92dd9-212">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="92dd9-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-213">Az.Sql</span></span>
* <span data-ttu-id="92dd9-214">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92dd9-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="92dd9-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-215">Az.Storage</span></span>
* <span data-ttu-id="92dd9-216">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="92dd9-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="92dd9-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="92dd9-217">New-AzStorageContext</span></span>
* <span data-ttu-id="92dd9-218">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="92dd9-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="92dd9-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="92dd9-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="92dd9-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="92dd9-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="92dd9-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="92dd9-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="92dd9-223">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="92dd9-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="92dd9-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="92dd9-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="92dd9-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="92dd9-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="92dd9-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="92dd9-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="92dd9-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="92dd9-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="92dd9-228">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="92dd9-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="92dd9-229">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="92dd9-229">Highlights since the last major release</span></span>
* <span data-ttu-id="92dd9-230">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="92dd9-230">General availability of `Az` module</span></span>
* <span data-ttu-id="92dd9-231">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="92dd9-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="92dd9-232">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="92dd9-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="92dd9-233">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="92dd9-234">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="92dd9-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="92dd9-235">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="92dd9-236">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="92dd9-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-237">Az.Automation</span></span>
* <span data-ttu-id="92dd9-238">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="92dd9-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="92dd9-239">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="92dd9-239">Dynamic grouping</span></span>
    * <span data-ttu-id="92dd9-240">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="92dd9-240">Pre-Post script</span></span>
    * <span data-ttu-id="92dd9-241">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="92dd9-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-242">Az.Compute</span></span>
* <span data-ttu-id="92dd9-243">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="92dd9-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="92dd9-244">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="92dd9-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="92dd9-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-245">Az.KeyVault</span></span>
* <span data-ttu-id="92dd9-246">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-247">Az.Network</span></span>
* <span data-ttu-id="92dd9-248">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="92dd9-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="92dd9-249">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="92dd9-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="92dd9-251">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="92dd9-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="92dd9-252">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="92dd9-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-253">Az.Resources</span></span>
* <span data-ttu-id="92dd9-254">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92dd9-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="92dd9-255">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="92dd9-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-256">Az.Sql</span></span>
* <span data-ttu-id="92dd9-257">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="92dd9-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="92dd9-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-258">Az.Storage</span></span>
* <span data-ttu-id="92dd9-259">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="92dd9-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="92dd9-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="92dd9-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="92dd9-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="92dd9-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="92dd9-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="92dd9-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="92dd9-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="92dd9-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="92dd9-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-266">Az.Websites</span></span>
* <span data-ttu-id="92dd9-267">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="92dd9-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="92dd9-268">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="92dd9-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="92dd9-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-269">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-270">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="92dd9-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="92dd9-271">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="92dd9-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-272">Az.Automation</span></span>
* <span data-ttu-id="92dd9-273">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="92dd9-274">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="92dd9-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="92dd9-275">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="92dd9-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="92dd9-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="92dd9-276">Az.Cdn</span></span>
* <span data-ttu-id="92dd9-277">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="92dd9-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-278">Az.Compute</span></span>
* <span data-ttu-id="92dd9-279">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="92dd9-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="92dd9-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="92dd9-280">Az.DataFactory</span></span>
* <span data-ttu-id="92dd9-281">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="92dd9-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="92dd9-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="92dd9-282">Az.LogicApp</span></span>
* <span data-ttu-id="92dd9-283">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="92dd9-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-284">Az.Network</span></span>
* <span data-ttu-id="92dd9-285">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="92dd9-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="92dd9-287">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="92dd9-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="92dd9-288">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="92dd9-288">SDK Update</span></span>
* <span data-ttu-id="92dd9-289">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="92dd9-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="92dd9-290">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="92dd9-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-291">Az.Resources</span></span>
* <span data-ttu-id="92dd9-292">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="92dd9-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="92dd9-293">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="92dd9-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="92dd9-294">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="92dd9-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="92dd9-295">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="92dd9-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="92dd9-296">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="92dd9-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="92dd9-297">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="92dd9-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-298">Az.Sql</span></span>
* <span data-ttu-id="92dd9-299">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="92dd9-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="92dd9-300">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="92dd9-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="92dd9-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-301">Az.Storage</span></span>
* <span data-ttu-id="92dd9-302">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="92dd9-303">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="92dd9-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="92dd9-305">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="92dd9-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-306">Az.Automation</span></span>
* <span data-ttu-id="92dd9-307">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="92dd9-308">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="92dd9-309">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="92dd9-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="92dd9-311">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="92dd9-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-312">Az.Compute</span></span>
* <span data-ttu-id="92dd9-313">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="92dd9-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="92dd9-314">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="92dd9-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="92dd9-315">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="92dd9-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="92dd9-316">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="92dd9-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-318">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="92dd9-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="92dd9-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-319">Az.EventHub</span></span>
* <span data-ttu-id="92dd9-320">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="92dd9-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="92dd9-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-321">Az.KeyVault</span></span>
* <span data-ttu-id="92dd9-322">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="92dd9-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="92dd9-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="92dd9-323">Az.LogicApp</span></span>
* <span data-ttu-id="92dd9-324">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="92dd9-325">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="92dd9-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="92dd9-326">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="92dd9-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="92dd9-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="92dd9-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="92dd9-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="92dd9-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="92dd9-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="92dd9-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="92dd9-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="92dd9-331">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="92dd9-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="92dd9-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="92dd9-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="92dd9-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="92dd9-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="92dd9-336">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="92dd9-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="92dd9-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="92dd9-337">Az.Monitor</span></span>
* <span data-ttu-id="92dd9-338">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="92dd9-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-339">Az.Network</span></span>
* <span data-ttu-id="92dd9-340">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="92dd9-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="92dd9-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="92dd9-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="92dd9-342">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="92dd9-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="92dd9-343">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="92dd9-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="92dd9-344">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="92dd9-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="92dd9-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-345">Az.Resources</span></span>
* <span data-ttu-id="92dd9-346">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="92dd9-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="92dd9-347">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="92dd9-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="92dd9-348">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="92dd9-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="92dd9-349">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="92dd9-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-350">Az.Sql</span></span>
* <span data-ttu-id="92dd9-351">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="92dd9-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="92dd9-352">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="92dd9-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-353">Az.Websites</span></span>
* <span data-ttu-id="92dd9-354">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="92dd9-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="92dd9-355">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="92dd9-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-356">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-357">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="92dd9-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="92dd9-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-358">Az.AnalysisServices</span></span>
<span data-ttu-id="92dd9-359">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="92dd9-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-360">Az.Compute</span></span>
* <span data-ttu-id="92dd9-361">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="92dd9-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="92dd9-362">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="92dd9-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="92dd9-363">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="92dd9-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-364">Az.RecoveryServices</span></span>
<span data-ttu-id="92dd9-365">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="92dd9-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-366">Az.Resources</span></span>
* <span data-ttu-id="92dd9-367">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="92dd9-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="92dd9-368">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="92dd9-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="92dd9-369">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="92dd9-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="92dd9-370">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="92dd9-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-371">Az.Sql</span></span>
* <span data-ttu-id="92dd9-372">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="92dd9-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="92dd9-373">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="92dd9-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="92dd9-374">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="92dd9-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="92dd9-375">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="92dd9-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-376">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-377">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="92dd9-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="92dd9-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="92dd9-379">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="92dd9-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="92dd9-381">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="92dd9-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="92dd9-382">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="92dd9-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-383">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-384">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="92dd9-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="92dd9-385">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="92dd9-386">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="92dd9-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="92dd9-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="92dd9-387">Az.Aks</span></span>
* <span data-ttu-id="92dd9-388">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="92dd9-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-389">Az.Automation</span></span>
* <span data-ttu-id="92dd9-390">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="92dd9-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="92dd9-391">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="92dd9-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="92dd9-392">Az.Cdn</span></span>
* <span data-ttu-id="92dd9-393">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-394">Az.Compute</span></span>
* <span data-ttu-id="92dd9-395">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="92dd9-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="92dd9-396">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="92dd9-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="92dd9-397">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="92dd9-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="92dd9-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="92dd9-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="92dd9-399">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="92dd9-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="92dd9-400">Az.DataFactory</span></span>
* <span data-ttu-id="92dd9-401">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="92dd9-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-403">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="92dd9-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="92dd9-404">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="92dd9-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="92dd9-405">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="92dd9-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-406">Az.IotHub</span></span>
* <span data-ttu-id="92dd9-407">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="92dd9-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="92dd9-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-408">Az.KeyVault</span></span>
* <span data-ttu-id="92dd9-409">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-410">Az.Network</span></span>
* <span data-ttu-id="92dd9-411">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-412">Az.Resources</span></span>
* <span data-ttu-id="92dd9-413">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="92dd9-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="92dd9-414">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="92dd9-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="92dd9-415">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92dd9-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="92dd9-416">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="92dd9-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="92dd9-417">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="92dd9-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="92dd9-418">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92dd9-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="92dd9-419">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="92dd9-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="92dd9-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92dd9-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="92dd9-421">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="92dd9-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="92dd9-422">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="92dd9-422">Fix some error messages.</span></span>
* <span data-ttu-id="92dd9-423">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92dd9-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="92dd9-424">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="92dd9-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="92dd9-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="92dd9-425">Az.SignalR</span></span>
* <span data-ttu-id="92dd9-426">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-427">Az.Sql</span></span>
* <span data-ttu-id="92dd9-428">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="92dd9-429">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="92dd9-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="92dd9-430">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="92dd9-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="92dd9-431">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="92dd9-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="92dd9-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-432">Az.Storage</span></span>
* <span data-ttu-id="92dd9-433">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="92dd9-434">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="92dd9-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="92dd9-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="92dd9-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="92dd9-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="92dd9-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="92dd9-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="92dd9-437">Az.TrafficManager</span></span>
* <span data-ttu-id="92dd9-438">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-439">Az.Websites</span></span>
* <span data-ttu-id="92dd9-440">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="92dd9-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="92dd9-441">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="92dd9-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="92dd9-442">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="92dd9-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="92dd9-443">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="92dd9-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-444">Az.Accounts</span></span>
* <span data-ttu-id="92dd9-445">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="92dd9-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-446">Az.Compute</span></span>
* <span data-ttu-id="92dd9-447">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="92dd9-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="92dd9-448">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="92dd9-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="92dd9-449">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-451">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="92dd9-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="92dd9-452">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="92dd9-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="92dd9-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="92dd9-453">Az.EventGrid</span></span>
* <span data-ttu-id="92dd9-454">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="92dd9-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="92dd9-455">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="92dd9-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="92dd9-456">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="92dd9-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="92dd9-457">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="92dd9-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="92dd9-458">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="92dd9-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="92dd9-459">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="92dd9-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="92dd9-460">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="92dd9-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="92dd9-461">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="92dd9-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="92dd9-462">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="92dd9-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="92dd9-463">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="92dd9-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="92dd9-464">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="92dd9-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="92dd9-465">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92dd9-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="92dd9-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-466">Az.IotHub</span></span>
* <span data-ttu-id="92dd9-467">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="92dd9-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="92dd9-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="92dd9-468">Az.LogicApp</span></span>
* <span data-ttu-id="92dd9-469">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="92dd9-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-470">Az.Resources</span></span>
* <span data-ttu-id="92dd9-471">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="92dd9-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="92dd9-472">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="92dd9-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="92dd9-473">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92dd9-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="92dd9-474">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="92dd9-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="92dd9-475">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="92dd9-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="92dd9-476">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="92dd9-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="92dd9-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="92dd9-477">Az.SignalR</span></span>
* <span data-ttu-id="92dd9-478">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-479">Az.Sql</span></span>
* <span data-ttu-id="92dd9-480">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="92dd9-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="92dd9-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-481">Az.Storage</span></span>
* <span data-ttu-id="92dd9-482">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="92dd9-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="92dd9-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="92dd9-483">New-AzStorageContext</span></span>
* <span data-ttu-id="92dd9-484">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="92dd9-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="92dd9-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="92dd9-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-486">Az.Websites</span></span>
* <span data-ttu-id="92dd9-487">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="92dd9-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="92dd9-488">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="92dd9-489">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="92dd9-490">Ogólne</span><span class="sxs-lookup"><span data-stu-id="92dd9-490">General</span></span>

- <span data-ttu-id="92dd9-491">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="92dd9-491">General Availability of Az Module</span></span>
- <span data-ttu-id="92dd9-492">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="92dd9-492">Online help for each module</span></span>
- <span data-ttu-id="92dd9-493">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="92dd9-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="92dd9-494">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="92dd9-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="92dd9-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-495">Az.Accounts</span></span>
- <span data-ttu-id="92dd9-496">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="92dd9-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="92dd9-497">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="92dd9-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="92dd9-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="92dd9-498">Az.ApiManagement</span></span>
- <span data-ttu-id="92dd9-499">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="92dd9-499">Fixes for #7002</span></span>
- <span data-ttu-id="92dd9-500">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="92dd9-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="92dd9-501">Az.Batch</span></span>
- <span data-ttu-id="92dd9-502">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="92dd9-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="92dd9-503">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="92dd9-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="92dd9-504">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="92dd9-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="92dd9-505">Az.Billing</span></span>
- <span data-ttu-id="92dd9-506">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="92dd9-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-507">Az.CognitivServices</span></span>
- <span data-ttu-id="92dd9-508">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="92dd9-509">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="92dd9-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="92dd9-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="92dd9-511">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="92dd9-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="92dd9-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="92dd9-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="92dd9-513">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="92dd9-515">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="92dd9-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="92dd9-516">Az.Monitor</span></span>
- <span data-ttu-id="92dd9-517">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="92dd9-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92dd9-518">Az.KeyVault</span></span>
- <span data-ttu-id="92dd9-519">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="92dd9-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="92dd9-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="92dd9-520">Az.MachineLearning</span></span>
- <span data-ttu-id="92dd9-521">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="92dd9-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="92dd9-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="92dd9-522">Az.Media</span></span>
- <span data-ttu-id="92dd9-523">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="92dd9-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="92dd9-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-524">Az.Network</span></span>
<span data-ttu-id="92dd9-525">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="92dd9-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="92dd9-526">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="92dd9-526">New cmdlets added:</span></span>
        - <span data-ttu-id="92dd9-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="92dd9-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="92dd9-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="92dd9-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="92dd9-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="92dd9-535">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92dd9-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="92dd9-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92dd9-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="92dd9-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="92dd9-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="92dd9-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="92dd9-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="92dd9-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="92dd9-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="92dd9-541">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="92dd9-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="92dd9-542">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="92dd9-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="92dd9-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92dd9-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="92dd9-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92dd9-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="92dd9-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92dd9-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="92dd9-546">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="92dd9-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="92dd9-547">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="92dd9-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="92dd9-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="92dd9-549">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="92dd9-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="92dd9-550">Az.Profile</span></span>
- <span data-ttu-id="92dd9-551">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="92dd9-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="92dd9-553">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="92dd9-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-554">Az.Resources</span></span>
- <span data-ttu-id="92dd9-555">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="92dd9-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92dd9-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="92dd9-557">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="92dd9-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="92dd9-558">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="92dd9-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="92dd9-559">Az.SIgnalR</span></span>
- <span data-ttu-id="92dd9-560">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="92dd9-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="92dd9-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-561">Az.Sql</span></span>
- <span data-ttu-id="92dd9-562">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="92dd9-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="92dd9-563">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="92dd9-564">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="92dd9-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-565">Az.Storage</span></span>
- <span data-ttu-id="92dd9-566">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="92dd9-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-567">Az.Websites</span></span>
- <span data-ttu-id="92dd9-568">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="92dd9-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="92dd9-569">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="92dd9-570">Ogólne</span><span class="sxs-lookup"><span data-stu-id="92dd9-570">General</span></span>

* <span data-ttu-id="92dd9-571">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="92dd9-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="92dd9-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-572">Az.Compute</span></span>

* <span data-ttu-id="92dd9-573">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="92dd9-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="92dd9-575">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="92dd9-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="92dd9-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="92dd9-576">Az.FrontDoor</span></span>

* <span data-ttu-id="92dd9-577">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="92dd9-577">Fixed some broken links</span></span>
    - <span data-ttu-id="92dd9-578">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="92dd9-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="92dd9-579">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="92dd9-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="92dd9-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="92dd9-581">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92dd9-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="92dd9-582">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92dd9-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="92dd9-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-583">Az.Resources</span></span>

* <span data-ttu-id="92dd9-584">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="92dd9-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="92dd9-585">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="92dd9-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="92dd9-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-586">Az.Sql</span></span>

* <span data-ttu-id="92dd9-587">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="92dd9-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="92dd9-588">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="92dd9-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="92dd9-589">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="92dd9-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="92dd9-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-590">Az.Storage</span></span>

* <span data-ttu-id="92dd9-591">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="92dd9-592">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="92dd9-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="92dd9-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="92dd9-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="92dd9-594">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="92dd9-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="92dd9-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="92dd9-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="92dd9-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="92dd9-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="92dd9-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-597">Az.Websites</span></span>

* <span data-ttu-id="92dd9-598">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="92dd9-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="92dd9-599">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="92dd9-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="92dd9-600">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="92dd9-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="92dd9-601">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="92dd9-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="92dd9-602">Az.ApiManagement</span></span>
* <span data-ttu-id="92dd9-603">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="92dd9-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="92dd9-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="92dd9-604">Az.Automation</span></span>
* <span data-ttu-id="92dd9-605">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="92dd9-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="92dd9-606">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="92dd9-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="92dd9-607">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="92dd9-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="92dd9-608">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="92dd9-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="92dd9-609">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="92dd9-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="92dd9-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-610">Az.Compute</span></span>
* <span data-ttu-id="92dd9-611">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="92dd9-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="92dd9-612">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="92dd9-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="92dd9-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="92dd9-614">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="92dd9-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="92dd9-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="92dd9-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="92dd9-616">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="92dd9-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="92dd9-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-617">Az.Network</span></span>
* <span data-ttu-id="92dd9-618">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="92dd9-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="92dd9-619">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="92dd9-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="92dd9-620">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="92dd9-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="92dd9-621">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92dd9-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="92dd9-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="92dd9-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="92dd9-623">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="92dd9-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="92dd9-624">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="92dd9-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="92dd9-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="92dd9-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="92dd9-626">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="92dd9-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="92dd9-627">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="92dd9-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="92dd9-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="92dd9-628">Az.Relay</span></span>
* <span data-ttu-id="92dd9-629">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="92dd9-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="92dd9-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-630">Az.Resources</span></span>
* <span data-ttu-id="92dd9-631">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="92dd9-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="92dd9-632">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="92dd9-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="92dd9-633">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="92dd9-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="92dd9-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92dd9-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="92dd9-635">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="92dd9-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="92dd9-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-636">Az.Sql</span></span>
* <span data-ttu-id="92dd9-637">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="92dd9-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="92dd9-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="92dd9-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="92dd9-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="92dd9-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="92dd9-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="92dd9-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="92dd9-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="92dd9-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="92dd9-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="92dd9-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="92dd9-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="92dd9-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="92dd9-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="92dd9-646">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="92dd9-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="92dd9-647">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="92dd9-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="92dd9-648">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="92dd9-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="92dd9-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="92dd9-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="92dd9-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="92dd9-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="92dd9-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="92dd9-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="92dd9-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="92dd9-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="92dd9-653">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="92dd9-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="92dd9-654">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="92dd9-655">Ogólne</span><span class="sxs-lookup"><span data-stu-id="92dd9-655">General</span></span>
* <span data-ttu-id="92dd9-656">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="92dd9-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="92dd9-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="92dd9-657">Az.Profile</span></span>
* <span data-ttu-id="92dd9-658">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="92dd9-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="92dd9-659">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="92dd9-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="92dd9-660">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="92dd9-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="92dd9-661">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="92dd9-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="92dd9-662">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="92dd9-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="92dd9-663">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="92dd9-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="92dd9-664">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="92dd9-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="92dd9-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="92dd9-666">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="92dd9-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-667">Az.Compute</span></span>
* <span data-ttu-id="92dd9-668">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="92dd9-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="92dd9-669">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="92dd9-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="92dd9-670">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="92dd9-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-672">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="92dd9-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="92dd9-673">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="92dd9-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="92dd9-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="92dd9-674">Az.Insights</span></span>
* <span data-ttu-id="92dd9-675">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="92dd9-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="92dd9-676">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="92dd9-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="92dd9-677">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="92dd9-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="92dd9-678">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="92dd9-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-679">Az.Network</span></span>
* <span data-ttu-id="92dd9-680">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="92dd9-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="92dd9-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="92dd9-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="92dd9-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="92dd9-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="92dd9-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="92dd9-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="92dd9-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="92dd9-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="92dd9-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="92dd9-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="92dd9-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="92dd9-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="92dd9-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="92dd9-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="92dd9-688">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="92dd9-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-689">Az.Resources</span></span>
* <span data-ttu-id="92dd9-690">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="92dd9-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="92dd9-691">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="92dd9-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="92dd9-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="92dd9-692">Az.ServiceBus</span></span>
* <span data-ttu-id="92dd9-693">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="92dd9-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="92dd9-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92dd9-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="92dd9-695">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="92dd9-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="92dd9-696">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="92dd9-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="92dd9-697">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="92dd9-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="92dd9-698">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="92dd9-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="92dd9-699">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="92dd9-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="92dd9-700">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="92dd9-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="92dd9-701">Az.Profile</span></span>
* <span data-ttu-id="92dd9-702">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="92dd9-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="92dd9-703">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="92dd9-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-704">Az.Compute</span></span>
* <span data-ttu-id="92dd9-705">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="92dd9-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="92dd9-706">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92dd9-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="92dd9-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92dd9-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="92dd9-708">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="92dd9-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="92dd9-709">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92dd9-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="92dd9-710">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92dd9-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="92dd9-711">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92dd9-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="92dd9-712">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92dd9-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-713">Az.Network</span></span>
* <span data-ttu-id="92dd9-714">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="92dd9-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="92dd9-715">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92dd9-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-716">Az.Resources</span></span>
* <span data-ttu-id="92dd9-717">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="92dd9-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="92dd9-718">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="92dd9-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="92dd9-719">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="92dd9-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="92dd9-720">Azure.Storage</span></span>
* <span data-ttu-id="92dd9-721">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="92dd9-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="92dd9-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="92dd9-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="92dd9-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="92dd9-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="92dd9-724">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="92dd9-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="92dd9-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="92dd9-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="92dd9-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="92dd9-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="92dd9-727">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="92dd9-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="92dd9-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="92dd9-728">Az.Compute</span></span>
* <span data-ttu-id="92dd9-729">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="92dd9-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="92dd9-730">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="92dd9-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="92dd9-731">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="92dd9-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="92dd9-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="92dd9-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="92dd9-733">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="92dd9-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="92dd9-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="92dd9-734">Az.Network</span></span>
* <span data-ttu-id="92dd9-735">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="92dd9-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="92dd9-736">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="92dd9-736">new cmdlets added</span></span>
    - <span data-ttu-id="92dd9-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="92dd9-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="92dd9-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="92dd9-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="92dd9-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="92dd9-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="92dd9-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="92dd9-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="92dd9-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="92dd9-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="92dd9-743">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="92dd9-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="92dd9-744">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="92dd9-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="92dd9-745">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="92dd9-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="92dd9-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="92dd9-746">Az.RedisCache</span></span>
* <span data-ttu-id="92dd9-747">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="92dd9-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="92dd9-748">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="92dd9-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="92dd9-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="92dd9-749">Az.Resources</span></span>
* <span data-ttu-id="92dd9-750">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92dd9-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="92dd9-751">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="92dd9-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="92dd9-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="92dd9-752">Az.Sql</span></span>
* <span data-ttu-id="92dd9-753">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="92dd9-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="92dd9-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="92dd9-754">Az.Websites</span></span>
* <span data-ttu-id="92dd9-755">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="92dd9-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="92dd9-756">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="92dd9-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="92dd9-757">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="92dd9-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="92dd9-758">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="92dd9-758">Initial Release</span></span>