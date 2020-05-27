---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386973"
---
## <a name="180---april-2019"></a><span data-ttu-id="557b3-103">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="557b3-104">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="557b3-104">Highlights since the last major release</span></span>
* <span data-ttu-id="557b3-105">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="557b3-105">General availability of `Az` module</span></span>
* <span data-ttu-id="557b3-106">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="557b3-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="557b3-107">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="557b3-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="557b3-108">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="557b3-109">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="557b3-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="557b3-110">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="557b3-111">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="557b3-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-112">Az.Accounts</span></span>
* <span data-ttu-id="557b3-113">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="557b3-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="557b3-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="557b3-114">Az.Batch</span></span>
* <span data-ttu-id="557b3-115">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="557b3-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="557b3-116">Az.Cdn</span></span>
* <span data-ttu-id="557b3-117">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="557b3-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="557b3-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="557b3-119">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-120">Az.Compute</span></span>
* <span data-ttu-id="557b3-121">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="557b3-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="557b3-122">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-123">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="557b3-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="557b3-124">Az.DataFactory</span></span>
* <span data-ttu-id="557b3-125">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="557b3-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-127">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="557b3-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="557b3-128">Az.EventGrid</span></span>
* <span data-ttu-id="557b3-129">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="557b3-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="557b3-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="557b3-130">Az.EventHub</span></span>
* <span data-ttu-id="557b3-131">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="557b3-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="557b3-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="557b3-132">Az.HDInsight</span></span>
* <span data-ttu-id="557b3-133">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="557b3-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="557b3-134">Az.IotHub</span></span>
* <span data-ttu-id="557b3-135">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="557b3-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-136">Az.KeyVault</span></span>
* <span data-ttu-id="557b3-137">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-138">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="557b3-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="557b3-139">Az.MachineLearning</span></span>
* <span data-ttu-id="557b3-140">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="557b3-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="557b3-141">Az.Media</span></span>
* <span data-ttu-id="557b3-142">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="557b3-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="557b3-143">Az.Monitor</span></span>
  * <span data-ttu-id="557b3-144">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="557b3-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="557b3-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="557b3-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="557b3-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="557b3-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="557b3-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="557b3-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="557b3-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="557b3-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="557b3-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="557b3-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="557b3-150">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="557b3-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-151">Az.Network</span></span>
* <span data-ttu-id="557b3-152">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-153">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="557b3-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="557b3-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="557b3-155">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="557b3-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="557b3-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="557b3-157">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="557b3-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="557b3-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="557b3-159">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="557b3-161">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-162">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="557b3-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="557b3-163">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="557b3-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="557b3-164">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="557b3-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="557b3-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="557b3-165">Az.RedisCache</span></span>
* <span data-ttu-id="557b3-166">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-167">Az.Resources</span></span>
* <span data-ttu-id="557b3-168">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-169">Az.Sql</span></span>
* <span data-ttu-id="557b3-170">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="557b3-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="557b3-171">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-172">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="557b3-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="557b3-173">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="557b3-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="557b3-174">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="557b3-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="557b3-175">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="557b3-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="557b3-176">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-177">Az.Websites</span></span>
* <span data-ttu-id="557b3-178">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="557b3-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="557b3-179">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="557b3-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="557b3-180">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="557b3-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="557b3-181">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="557b3-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="557b3-182">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="557b3-183">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="557b3-183">Highlights since the last major release</span></span>
* <span data-ttu-id="557b3-184">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="557b3-184">General availability of `Az` module</span></span>
* <span data-ttu-id="557b3-185">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="557b3-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="557b3-186">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="557b3-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="557b3-187">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="557b3-188">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="557b3-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="557b3-189">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="557b3-190">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="557b3-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-191">Az.Accounts</span></span>
* <span data-ttu-id="557b3-192">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="557b3-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="557b3-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="557b3-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="557b3-194">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="557b3-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="557b3-195">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="557b3-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="557b3-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-196">Az.Automation</span></span>
* <span data-ttu-id="557b3-197">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="557b3-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="557b3-198">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="557b3-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="557b3-199">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-200">Az.Compute</span></span>
* <span data-ttu-id="557b3-201">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="557b3-202">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="557b3-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="557b3-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="557b3-204">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="557b3-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="557b3-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="557b3-205">Az.DataFactory</span></span>
* <span data-ttu-id="557b3-206">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="557b3-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="557b3-207">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="557b3-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-208">Az.Resources</span></span>
* <span data-ttu-id="557b3-209">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="557b3-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="557b3-210">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="557b3-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="557b3-211">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="557b3-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="557b3-212">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="557b3-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="557b3-213">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="557b3-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="557b3-214">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="557b3-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-215">Az.Sql</span></span>
* <span data-ttu-id="557b3-216">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="557b3-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="557b3-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-217">Az.Storage</span></span>
* <span data-ttu-id="557b3-218">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="557b3-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="557b3-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="557b3-219">New-AzStorageContext</span></span>
* <span data-ttu-id="557b3-220">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="557b3-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="557b3-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="557b3-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="557b3-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="557b3-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="557b3-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="557b3-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="557b3-225">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="557b3-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="557b3-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="557b3-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="557b3-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="557b3-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="557b3-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="557b3-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="557b3-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="557b3-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="557b3-230">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="557b3-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="557b3-231">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="557b3-231">Highlights since the last major release</span></span>
* <span data-ttu-id="557b3-232">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="557b3-232">General availability of `Az` module</span></span>
* <span data-ttu-id="557b3-233">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="557b3-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="557b3-234">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="557b3-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="557b3-235">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="557b3-236">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="557b3-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="557b3-237">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="557b3-238">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="557b3-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-239">Az.Automation</span></span>
* <span data-ttu-id="557b3-240">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="557b3-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="557b3-241">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="557b3-241">Dynamic grouping</span></span>
    * <span data-ttu-id="557b3-242">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="557b3-242">Pre-Post script</span></span>
    * <span data-ttu-id="557b3-243">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="557b3-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-244">Az.Compute</span></span>
* <span data-ttu-id="557b3-245">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="557b3-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="557b3-246">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="557b3-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="557b3-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-247">Az.KeyVault</span></span>
* <span data-ttu-id="557b3-248">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-249">Az.Network</span></span>
* <span data-ttu-id="557b3-250">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="557b3-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="557b3-251">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="557b3-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="557b3-253">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="557b3-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="557b3-254">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="557b3-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-255">Az.Resources</span></span>
* <span data-ttu-id="557b3-256">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="557b3-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="557b3-257">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="557b3-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-258">Az.Sql</span></span>
* <span data-ttu-id="557b3-259">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="557b3-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="557b3-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-260">Az.Storage</span></span>
* <span data-ttu-id="557b3-261">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="557b3-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="557b3-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="557b3-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="557b3-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="557b3-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="557b3-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="557b3-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="557b3-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="557b3-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="557b3-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-268">Az.Websites</span></span>
* <span data-ttu-id="557b3-269">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="557b3-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="557b3-270">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="557b3-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="557b3-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-271">Az.Accounts</span></span>
* <span data-ttu-id="557b3-272">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="557b3-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="557b3-273">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="557b3-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-274">Az.Automation</span></span>
* <span data-ttu-id="557b3-275">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="557b3-276">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="557b3-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="557b3-277">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="557b3-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="557b3-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="557b3-278">Az.Cdn</span></span>
* <span data-ttu-id="557b3-279">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="557b3-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-280">Az.Compute</span></span>
* <span data-ttu-id="557b3-281">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="557b3-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="557b3-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="557b3-282">Az.DataFactory</span></span>
* <span data-ttu-id="557b3-283">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="557b3-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="557b3-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="557b3-284">Az.LogicApp</span></span>
* <span data-ttu-id="557b3-285">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="557b3-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-286">Az.Network</span></span>
* <span data-ttu-id="557b3-287">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="557b3-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="557b3-289">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="557b3-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="557b3-290">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="557b3-290">SDK Update</span></span>
* <span data-ttu-id="557b3-291">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="557b3-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="557b3-292">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="557b3-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-293">Az.Resources</span></span>
* <span data-ttu-id="557b3-294">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="557b3-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="557b3-295">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="557b3-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="557b3-296">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="557b3-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="557b3-297">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="557b3-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="557b3-298">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="557b3-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="557b3-299">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="557b3-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-300">Az.Sql</span></span>
* <span data-ttu-id="557b3-301">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="557b3-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="557b3-302">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="557b3-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="557b3-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-303">Az.Storage</span></span>
* <span data-ttu-id="557b3-304">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="557b3-305">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="557b3-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="557b3-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="557b3-307">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="557b3-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-308">Az.Automation</span></span>
* <span data-ttu-id="557b3-309">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="557b3-310">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="557b3-311">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="557b3-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="557b3-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="557b3-313">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="557b3-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-314">Az.Compute</span></span>
* <span data-ttu-id="557b3-315">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="557b3-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="557b3-316">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="557b3-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="557b3-317">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="557b3-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="557b3-318">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="557b3-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-320">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="557b3-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="557b3-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="557b3-321">Az.EventHub</span></span>
* <span data-ttu-id="557b3-322">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="557b3-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="557b3-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-323">Az.KeyVault</span></span>
* <span data-ttu-id="557b3-324">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="557b3-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="557b3-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="557b3-325">Az.LogicApp</span></span>
* <span data-ttu-id="557b3-326">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="557b3-327">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="557b3-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="557b3-328">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="557b3-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557b3-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="557b3-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557b3-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="557b3-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557b3-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="557b3-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557b3-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="557b3-333">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="557b3-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="557b3-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="557b3-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="557b3-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="557b3-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="557b3-338">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="557b3-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="557b3-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="557b3-339">Az.Monitor</span></span>
* <span data-ttu-id="557b3-340">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="557b3-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-341">Az.Network</span></span>
* <span data-ttu-id="557b3-342">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="557b3-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="557b3-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="557b3-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="557b3-344">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="557b3-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="557b3-345">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="557b3-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="557b3-346">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="557b3-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="557b3-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-347">Az.Resources</span></span>
* <span data-ttu-id="557b3-348">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="557b3-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="557b3-349">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="557b3-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="557b3-350">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="557b3-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="557b3-351">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="557b3-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-352">Az.Sql</span></span>
* <span data-ttu-id="557b3-353">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="557b3-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="557b3-354">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="557b3-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-355">Az.Websites</span></span>
* <span data-ttu-id="557b3-356">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="557b3-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="557b3-357">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="557b3-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-358">Az.Accounts</span></span>
* <span data-ttu-id="557b3-359">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="557b3-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="557b3-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="557b3-360">Az.AnalysisServices</span></span>
<span data-ttu-id="557b3-361">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="557b3-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-362">Az.Compute</span></span>
* <span data-ttu-id="557b3-363">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="557b3-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="557b3-364">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="557b3-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="557b3-365">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="557b3-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-366">Az.RecoveryServices</span></span>
<span data-ttu-id="557b3-367">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="557b3-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-368">Az.Resources</span></span>
* <span data-ttu-id="557b3-369">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="557b3-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="557b3-370">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="557b3-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="557b3-371">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="557b3-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="557b3-372">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="557b3-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-373">Az.Sql</span></span>
* <span data-ttu-id="557b3-374">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="557b3-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="557b3-375">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="557b3-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="557b3-376">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="557b3-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="557b3-377">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="557b3-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-378">Az.Accounts</span></span>
* <span data-ttu-id="557b3-379">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="557b3-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="557b3-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="557b3-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="557b3-381">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="557b3-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="557b3-383">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="557b3-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="557b3-384">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="557b3-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-385">Az.Accounts</span></span>
* <span data-ttu-id="557b3-386">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="557b3-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="557b3-387">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="557b3-388">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="557b3-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="557b3-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="557b3-389">Az.Aks</span></span>
* <span data-ttu-id="557b3-390">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="557b3-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-391">Az.Automation</span></span>
* <span data-ttu-id="557b3-392">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="557b3-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="557b3-393">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="557b3-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="557b3-394">Az.Cdn</span></span>
* <span data-ttu-id="557b3-395">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-396">Az.Compute</span></span>
* <span data-ttu-id="557b3-397">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="557b3-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="557b3-398">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="557b3-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="557b3-399">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="557b3-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="557b3-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="557b3-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="557b3-401">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="557b3-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="557b3-402">Az.DataFactory</span></span>
* <span data-ttu-id="557b3-403">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="557b3-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-405">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="557b3-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="557b3-406">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="557b3-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="557b3-407">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="557b3-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="557b3-408">Az.IotHub</span></span>
* <span data-ttu-id="557b3-409">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="557b3-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="557b3-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-410">Az.KeyVault</span></span>
* <span data-ttu-id="557b3-411">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-412">Az.Network</span></span>
* <span data-ttu-id="557b3-413">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-414">Az.Resources</span></span>
* <span data-ttu-id="557b3-415">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="557b3-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="557b3-416">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="557b3-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="557b3-417">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="557b3-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="557b3-418">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="557b3-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="557b3-419">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="557b3-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="557b3-420">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="557b3-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="557b3-421">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="557b3-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="557b3-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="557b3-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="557b3-423">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="557b3-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="557b3-424">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="557b3-424">Fix some error messages.</span></span>
* <span data-ttu-id="557b3-425">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="557b3-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="557b3-426">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="557b3-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="557b3-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="557b3-427">Az.SignalR</span></span>
* <span data-ttu-id="557b3-428">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-429">Az.Sql</span></span>
* <span data-ttu-id="557b3-430">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="557b3-431">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="557b3-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="557b3-432">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="557b3-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="557b3-433">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="557b3-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="557b3-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-434">Az.Storage</span></span>
* <span data-ttu-id="557b3-435">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="557b3-436">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="557b3-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="557b3-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="557b3-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="557b3-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="557b3-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="557b3-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="557b3-439">Az.TrafficManager</span></span>
* <span data-ttu-id="557b3-440">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-441">Az.Websites</span></span>
* <span data-ttu-id="557b3-442">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="557b3-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="557b3-443">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="557b3-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="557b3-444">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="557b3-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="557b3-445">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="557b3-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-446">Az.Accounts</span></span>
* <span data-ttu-id="557b3-447">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="557b3-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-448">Az.Compute</span></span>
* <span data-ttu-id="557b3-449">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="557b3-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="557b3-450">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="557b3-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="557b3-451">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-453">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="557b3-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="557b3-454">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="557b3-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="557b3-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="557b3-455">Az.EventGrid</span></span>
* <span data-ttu-id="557b3-456">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="557b3-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="557b3-457">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="557b3-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="557b3-458">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="557b3-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="557b3-459">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="557b3-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="557b3-460">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="557b3-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="557b3-461">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="557b3-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="557b3-462">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="557b3-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="557b3-463">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="557b3-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="557b3-464">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="557b3-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="557b3-465">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="557b3-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="557b3-466">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="557b3-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="557b3-467">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="557b3-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="557b3-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="557b3-468">Az.IotHub</span></span>
* <span data-ttu-id="557b3-469">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="557b3-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="557b3-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="557b3-470">Az.LogicApp</span></span>
* <span data-ttu-id="557b3-471">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="557b3-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-472">Az.Resources</span></span>
* <span data-ttu-id="557b3-473">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="557b3-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="557b3-474">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="557b3-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="557b3-475">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="557b3-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="557b3-476">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="557b3-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="557b3-477">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="557b3-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="557b3-478">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="557b3-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="557b3-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="557b3-479">Az.SignalR</span></span>
* <span data-ttu-id="557b3-480">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-481">Az.Sql</span></span>
* <span data-ttu-id="557b3-482">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="557b3-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="557b3-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-483">Az.Storage</span></span>
* <span data-ttu-id="557b3-484">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="557b3-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="557b3-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="557b3-485">New-AzStorageContext</span></span>
* <span data-ttu-id="557b3-486">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="557b3-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="557b3-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="557b3-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-488">Az.Websites</span></span>
* <span data-ttu-id="557b3-489">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="557b3-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="557b3-490">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="557b3-491">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="557b3-492">Ogólne</span><span class="sxs-lookup"><span data-stu-id="557b3-492">General</span></span>

- <span data-ttu-id="557b3-493">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="557b3-493">General Availability of Az Module</span></span>
- <span data-ttu-id="557b3-494">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="557b3-494">Online help for each module</span></span>
- <span data-ttu-id="557b3-495">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="557b3-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="557b3-496">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="557b3-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="557b3-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-497">Az.Accounts</span></span>
- <span data-ttu-id="557b3-498">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="557b3-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="557b3-499">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="557b3-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="557b3-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="557b3-500">Az.ApiManagement</span></span>
- <span data-ttu-id="557b3-501">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="557b3-501">Fixes for #7002</span></span>
- <span data-ttu-id="557b3-502">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="557b3-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="557b3-503">Az.Batch</span></span>
- <span data-ttu-id="557b3-504">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="557b3-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="557b3-505">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="557b3-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="557b3-506">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="557b3-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="557b3-507">Az.Billing</span></span>
- <span data-ttu-id="557b3-508">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="557b3-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="557b3-509">Az.CognitivServices</span></span>
- <span data-ttu-id="557b3-510">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="557b3-511">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="557b3-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="557b3-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="557b3-513">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="557b3-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="557b3-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="557b3-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="557b3-515">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="557b3-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="557b3-517">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="557b3-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="557b3-518">Az.Monitor</span></span>
- <span data-ttu-id="557b3-519">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="557b3-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="557b3-520">Az.KeyVault</span></span>
- <span data-ttu-id="557b3-521">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="557b3-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="557b3-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="557b3-522">Az.MachineLearning</span></span>
- <span data-ttu-id="557b3-523">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="557b3-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="557b3-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="557b3-524">Az.Media</span></span>
- <span data-ttu-id="557b3-525">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="557b3-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="557b3-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-526">Az.Network</span></span>
<span data-ttu-id="557b3-527">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="557b3-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="557b3-528">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="557b3-528">New cmdlets added:</span></span>
        - <span data-ttu-id="557b3-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="557b3-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="557b3-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="557b3-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="557b3-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="557b3-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="557b3-537">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="557b3-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="557b3-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="557b3-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="557b3-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="557b3-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="557b3-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="557b3-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="557b3-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="557b3-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="557b3-543">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="557b3-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="557b3-544">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="557b3-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="557b3-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="557b3-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="557b3-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="557b3-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="557b3-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="557b3-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="557b3-548">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="557b3-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="557b3-549">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="557b3-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="557b3-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="557b3-551">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="557b3-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="557b3-552">Az.Profile</span></span>
- <span data-ttu-id="557b3-553">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="557b3-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="557b3-555">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="557b3-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-556">Az.Resources</span></span>
- <span data-ttu-id="557b3-557">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="557b3-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="557b3-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="557b3-559">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="557b3-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="557b3-560">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="557b3-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="557b3-561">Az.SIgnalR</span></span>
- <span data-ttu-id="557b3-562">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="557b3-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="557b3-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-563">Az.Sql</span></span>
- <span data-ttu-id="557b3-564">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="557b3-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="557b3-565">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="557b3-566">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="557b3-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-567">Az.Storage</span></span>
- <span data-ttu-id="557b3-568">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="557b3-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-569">Az.Websites</span></span>
- <span data-ttu-id="557b3-570">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="557b3-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="557b3-571">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="557b3-572">Ogólne</span><span class="sxs-lookup"><span data-stu-id="557b3-572">General</span></span>

* <span data-ttu-id="557b3-573">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="557b3-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="557b3-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-574">Az.Compute</span></span>

* <span data-ttu-id="557b3-575">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="557b3-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="557b3-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="557b3-577">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="557b3-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="557b3-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="557b3-578">Az.FrontDoor</span></span>

* <span data-ttu-id="557b3-579">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="557b3-579">Fixed some broken links</span></span>
    - <span data-ttu-id="557b3-580">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="557b3-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="557b3-581">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="557b3-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="557b3-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="557b3-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="557b3-583">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="557b3-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="557b3-584">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="557b3-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="557b3-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-585">Az.Resources</span></span>

* <span data-ttu-id="557b3-586">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="557b3-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="557b3-587">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="557b3-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="557b3-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-588">Az.Sql</span></span>

* <span data-ttu-id="557b3-589">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="557b3-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="557b3-590">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="557b3-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="557b3-591">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="557b3-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="557b3-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-592">Az.Storage</span></span>

* <span data-ttu-id="557b3-593">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="557b3-594">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="557b3-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="557b3-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="557b3-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="557b3-596">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="557b3-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="557b3-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="557b3-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="557b3-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="557b3-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="557b3-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-599">Az.Websites</span></span>

* <span data-ttu-id="557b3-600">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="557b3-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="557b3-601">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="557b3-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="557b3-602">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="557b3-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="557b3-603">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="557b3-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="557b3-604">Az.ApiManagement</span></span>
* <span data-ttu-id="557b3-605">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="557b3-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="557b3-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="557b3-606">Az.Automation</span></span>
* <span data-ttu-id="557b3-607">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="557b3-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="557b3-608">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="557b3-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="557b3-609">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="557b3-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="557b3-610">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="557b3-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="557b3-611">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="557b3-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="557b3-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-612">Az.Compute</span></span>
* <span data-ttu-id="557b3-613">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="557b3-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="557b3-614">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="557b3-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="557b3-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="557b3-616">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="557b3-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="557b3-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="557b3-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="557b3-618">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="557b3-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="557b3-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-619">Az.Network</span></span>
* <span data-ttu-id="557b3-620">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="557b3-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="557b3-621">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="557b3-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="557b3-622">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="557b3-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="557b3-623">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="557b3-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="557b3-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="557b3-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="557b3-625">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="557b3-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="557b3-626">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="557b3-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="557b3-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="557b3-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="557b3-628">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="557b3-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="557b3-629">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="557b3-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="557b3-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="557b3-630">Az.Relay</span></span>
* <span data-ttu-id="557b3-631">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="557b3-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="557b3-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-632">Az.Resources</span></span>
* <span data-ttu-id="557b3-633">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="557b3-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="557b3-634">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="557b3-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="557b3-635">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="557b3-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="557b3-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="557b3-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="557b3-637">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="557b3-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="557b3-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-638">Az.Sql</span></span>
* <span data-ttu-id="557b3-639">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="557b3-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="557b3-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="557b3-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="557b3-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="557b3-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="557b3-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="557b3-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="557b3-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="557b3-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="557b3-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="557b3-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="557b3-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="557b3-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="557b3-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="557b3-648">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="557b3-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="557b3-649">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="557b3-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="557b3-650">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="557b3-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="557b3-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="557b3-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="557b3-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="557b3-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="557b3-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="557b3-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="557b3-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="557b3-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="557b3-655">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="557b3-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="557b3-656">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="557b3-657">Ogólne</span><span class="sxs-lookup"><span data-stu-id="557b3-657">General</span></span>
* <span data-ttu-id="557b3-658">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="557b3-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="557b3-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="557b3-659">Az.Profile</span></span>
* <span data-ttu-id="557b3-660">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="557b3-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="557b3-661">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="557b3-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="557b3-662">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="557b3-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="557b3-663">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="557b3-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="557b3-664">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="557b3-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="557b3-665">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="557b3-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="557b3-666">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="557b3-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="557b3-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="557b3-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="557b3-668">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="557b3-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-669">Az.Compute</span></span>
* <span data-ttu-id="557b3-670">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="557b3-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="557b3-671">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="557b3-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="557b3-672">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="557b3-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-674">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="557b3-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="557b3-675">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="557b3-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="557b3-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="557b3-676">Az.Insights</span></span>
* <span data-ttu-id="557b3-677">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="557b3-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="557b3-678">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="557b3-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="557b3-679">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="557b3-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="557b3-680">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="557b3-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-681">Az.Network</span></span>
* <span data-ttu-id="557b3-682">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="557b3-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="557b3-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="557b3-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="557b3-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="557b3-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="557b3-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="557b3-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="557b3-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="557b3-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="557b3-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="557b3-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="557b3-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="557b3-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="557b3-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="557b3-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="557b3-690">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="557b3-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-691">Az.Resources</span></span>
* <span data-ttu-id="557b3-692">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="557b3-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="557b3-693">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="557b3-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="557b3-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="557b3-694">Az.ServiceBus</span></span>
* <span data-ttu-id="557b3-695">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="557b3-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="557b3-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="557b3-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="557b3-697">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="557b3-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="557b3-698">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="557b3-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="557b3-699">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="557b3-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="557b3-700">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="557b3-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="557b3-701">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="557b3-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="557b3-702">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="557b3-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="557b3-703">Az.Profile</span></span>
* <span data-ttu-id="557b3-704">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="557b3-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="557b3-705">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="557b3-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-706">Az.Compute</span></span>
* <span data-ttu-id="557b3-707">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="557b3-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="557b3-708">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557b3-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="557b3-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="557b3-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="557b3-710">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="557b3-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="557b3-711">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="557b3-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="557b3-712">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="557b3-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="557b3-713">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="557b3-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="557b3-714">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="557b3-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-715">Az.Network</span></span>
* <span data-ttu-id="557b3-716">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="557b3-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="557b3-717">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557b3-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-718">Az.Resources</span></span>
* <span data-ttu-id="557b3-719">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="557b3-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="557b3-720">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="557b3-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="557b3-721">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="557b3-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="557b3-722">Azure.Storage</span></span>
* <span data-ttu-id="557b3-723">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="557b3-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="557b3-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="557b3-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="557b3-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="557b3-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="557b3-726">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="557b3-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="557b3-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="557b3-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="557b3-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="557b3-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="557b3-729">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="557b3-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="557b3-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="557b3-730">Az.Compute</span></span>
* <span data-ttu-id="557b3-731">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="557b3-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="557b3-732">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="557b3-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="557b3-733">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="557b3-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="557b3-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="557b3-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="557b3-735">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="557b3-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="557b3-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="557b3-736">Az.Network</span></span>
* <span data-ttu-id="557b3-737">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="557b3-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="557b3-738">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="557b3-738">new cmdlets added</span></span>
    - <span data-ttu-id="557b3-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="557b3-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="557b3-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="557b3-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="557b3-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="557b3-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="557b3-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="557b3-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="557b3-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="557b3-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="557b3-745">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="557b3-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="557b3-746">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="557b3-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="557b3-747">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="557b3-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="557b3-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="557b3-748">Az.RedisCache</span></span>
* <span data-ttu-id="557b3-749">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="557b3-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="557b3-750">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="557b3-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="557b3-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="557b3-751">Az.Resources</span></span>
* <span data-ttu-id="557b3-752">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="557b3-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="557b3-753">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="557b3-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="557b3-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="557b3-754">Az.Sql</span></span>
* <span data-ttu-id="557b3-755">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="557b3-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="557b3-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="557b3-756">Az.Websites</span></span>
* <span data-ttu-id="557b3-757">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="557b3-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="557b3-758">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="557b3-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="557b3-759">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="557b3-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="557b3-760">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="557b3-760">Initial Release</span></span>
