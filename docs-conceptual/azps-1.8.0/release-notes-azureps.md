---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319308"
---
## <a name="180---april-2019"></a><span data-ttu-id="a491f-103">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a491f-104">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="a491f-104">Highlights since the last major release</span></span>
* <span data-ttu-id="a491f-105">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="a491f-105">General availability of `Az` module</span></span>
* <span data-ttu-id="a491f-106">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a491f-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a491f-107">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a491f-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a491f-108">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a491f-109">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a491f-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a491f-110">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a491f-111">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a491f-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-112">Az.Accounts</span></span>
* <span data-ttu-id="a491f-113">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="a491f-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a491f-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a491f-114">Az.Batch</span></span>
* <span data-ttu-id="a491f-115">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a491f-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a491f-116">Az.Cdn</span></span>
* <span data-ttu-id="a491f-117">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a491f-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a491f-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="a491f-119">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-120">Az.Compute</span></span>
* <span data-ttu-id="a491f-121">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="a491f-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a491f-122">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-123">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a491f-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a491f-124">Az.DataFactory</span></span>
* <span data-ttu-id="a491f-125">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="a491f-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-127">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a491f-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a491f-128">Az.EventGrid</span></span>
* <span data-ttu-id="a491f-129">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="a491f-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a491f-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a491f-130">Az.EventHub</span></span>
* <span data-ttu-id="a491f-131">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="a491f-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a491f-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a491f-132">Az.HDInsight</span></span>
* <span data-ttu-id="a491f-133">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a491f-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a491f-134">Az.IotHub</span></span>
* <span data-ttu-id="a491f-135">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a491f-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-136">Az.KeyVault</span></span>
* <span data-ttu-id="a491f-137">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-138">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a491f-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a491f-139">Az.MachineLearning</span></span>
* <span data-ttu-id="a491f-140">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a491f-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a491f-141">Az.Media</span></span>
* <span data-ttu-id="a491f-142">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a491f-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a491f-143">Az.Monitor</span></span>
  * <span data-ttu-id="a491f-144">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="a491f-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a491f-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a491f-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a491f-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a491f-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a491f-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a491f-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a491f-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a491f-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a491f-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a491f-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a491f-150">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a491f-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-151">Az.Network</span></span>
* <span data-ttu-id="a491f-152">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-153">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a491f-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a491f-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="a491f-155">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a491f-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a491f-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="a491f-157">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a491f-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a491f-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a491f-159">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="a491f-161">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-162">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a491f-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a491f-163">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a491f-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a491f-164">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="a491f-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a491f-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a491f-165">Az.RedisCache</span></span>
* <span data-ttu-id="a491f-166">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-167">Az.Resources</span></span>
* <span data-ttu-id="a491f-168">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-169">Az.Sql</span></span>
* <span data-ttu-id="a491f-170">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="a491f-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a491f-171">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-172">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="a491f-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a491f-173">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="a491f-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a491f-174">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="a491f-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a491f-175">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="a491f-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a491f-176">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-177">Az.Websites</span></span>
* <span data-ttu-id="a491f-178">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="a491f-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a491f-179">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="a491f-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a491f-180">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="a491f-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a491f-181">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a491f-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a491f-182">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a491f-183">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="a491f-183">Highlights since the last major release</span></span>
* <span data-ttu-id="a491f-184">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="a491f-184">General availability of `Az` module</span></span>
* <span data-ttu-id="a491f-185">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a491f-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a491f-186">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a491f-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a491f-187">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a491f-188">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a491f-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a491f-189">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a491f-190">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a491f-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-191">Az.Accounts</span></span>
* <span data-ttu-id="a491f-192">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a491f-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a491f-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a491f-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="a491f-194">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a491f-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a491f-195">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="a491f-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a491f-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-196">Az.Automation</span></span>
* <span data-ttu-id="a491f-197">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="a491f-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a491f-198">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="a491f-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a491f-199">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-200">Az.Compute</span></span>
* <span data-ttu-id="a491f-201">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a491f-202">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="a491f-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a491f-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="a491f-204">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="a491f-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a491f-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a491f-205">Az.DataFactory</span></span>
* <span data-ttu-id="a491f-206">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a491f-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a491f-207">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a491f-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-208">Az.Resources</span></span>
* <span data-ttu-id="a491f-209">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="a491f-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a491f-210">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a491f-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a491f-211">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="a491f-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a491f-212">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a491f-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a491f-213">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="a491f-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a491f-214">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a491f-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-215">Az.Sql</span></span>
* <span data-ttu-id="a491f-216">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a491f-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a491f-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-217">Az.Storage</span></span>
* <span data-ttu-id="a491f-218">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a491f-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a491f-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a491f-219">New-AzStorageContext</span></span>
* <span data-ttu-id="a491f-220">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="a491f-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a491f-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a491f-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a491f-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a491f-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a491f-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a491f-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a491f-225">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="a491f-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a491f-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a491f-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a491f-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a491f-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a491f-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a491f-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a491f-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a491f-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a491f-230">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="a491f-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a491f-231">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="a491f-231">Highlights since the last major release</span></span>
* <span data-ttu-id="a491f-232">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="a491f-232">General availability of `Az` module</span></span>
* <span data-ttu-id="a491f-233">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a491f-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a491f-234">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a491f-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a491f-235">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a491f-236">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a491f-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a491f-237">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a491f-238">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a491f-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-239">Az.Automation</span></span>
* <span data-ttu-id="a491f-240">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="a491f-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a491f-241">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="a491f-241">Dynamic grouping</span></span>
    * <span data-ttu-id="a491f-242">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="a491f-242">Pre-Post script</span></span>
    * <span data-ttu-id="a491f-243">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="a491f-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-244">Az.Compute</span></span>
* <span data-ttu-id="a491f-245">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a491f-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a491f-246">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a491f-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a491f-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-247">Az.KeyVault</span></span>
* <span data-ttu-id="a491f-248">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-249">Az.Network</span></span>
* <span data-ttu-id="a491f-250">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="a491f-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a491f-251">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="a491f-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="a491f-253">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="a491f-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a491f-254">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="a491f-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-255">Az.Resources</span></span>
* <span data-ttu-id="a491f-256">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a491f-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a491f-257">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="a491f-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-258">Az.Sql</span></span>
* <span data-ttu-id="a491f-259">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="a491f-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a491f-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-260">Az.Storage</span></span>
* <span data-ttu-id="a491f-261">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="a491f-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a491f-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a491f-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a491f-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a491f-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a491f-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a491f-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a491f-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a491f-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a491f-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-268">Az.Websites</span></span>
* <span data-ttu-id="a491f-269">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="a491f-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a491f-270">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="a491f-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a491f-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-271">Az.Accounts</span></span>
* <span data-ttu-id="a491f-272">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="a491f-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a491f-273">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a491f-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-274">Az.Automation</span></span>
* <span data-ttu-id="a491f-275">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a491f-276">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="a491f-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a491f-277">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="a491f-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a491f-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a491f-278">Az.Cdn</span></span>
* <span data-ttu-id="a491f-279">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="a491f-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-280">Az.Compute</span></span>
* <span data-ttu-id="a491f-281">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="a491f-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a491f-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a491f-282">Az.DataFactory</span></span>
* <span data-ttu-id="a491f-283">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a491f-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a491f-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a491f-284">Az.LogicApp</span></span>
* <span data-ttu-id="a491f-285">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="a491f-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-286">Az.Network</span></span>
* <span data-ttu-id="a491f-287">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="a491f-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="a491f-289">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a491f-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a491f-290">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="a491f-290">SDK Update</span></span>
* <span data-ttu-id="a491f-291">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a491f-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a491f-292">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a491f-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-293">Az.Resources</span></span>
* <span data-ttu-id="a491f-294">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="a491f-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a491f-295">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a491f-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a491f-296">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a491f-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a491f-297">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a491f-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a491f-298">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a491f-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a491f-299">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a491f-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-300">Az.Sql</span></span>
* <span data-ttu-id="a491f-301">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a491f-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a491f-302">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="a491f-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a491f-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-303">Az.Storage</span></span>
* <span data-ttu-id="a491f-304">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a491f-305">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a491f-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a491f-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="a491f-307">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a491f-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-308">Az.Automation</span></span>
* <span data-ttu-id="a491f-309">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a491f-310">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a491f-311">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a491f-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a491f-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="a491f-313">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="a491f-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-314">Az.Compute</span></span>
* <span data-ttu-id="a491f-315">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="a491f-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a491f-316">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="a491f-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a491f-317">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a491f-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a491f-318">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a491f-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-320">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="a491f-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a491f-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a491f-321">Az.EventHub</span></span>
* <span data-ttu-id="a491f-322">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="a491f-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a491f-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-323">Az.KeyVault</span></span>
* <span data-ttu-id="a491f-324">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a491f-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a491f-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a491f-325">Az.LogicApp</span></span>
* <span data-ttu-id="a491f-326">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a491f-327">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="a491f-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a491f-328">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a491f-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a491f-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a491f-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a491f-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a491f-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a491f-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a491f-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a491f-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a491f-333">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="a491f-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a491f-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a491f-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a491f-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a491f-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a491f-338">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a491f-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a491f-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a491f-339">Az.Monitor</span></span>
* <span data-ttu-id="a491f-340">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a491f-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-341">Az.Network</span></span>
* <span data-ttu-id="a491f-342">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a491f-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a491f-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a491f-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="a491f-344">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a491f-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a491f-345">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a491f-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a491f-346">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="a491f-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a491f-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-347">Az.Resources</span></span>
* <span data-ttu-id="a491f-348">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a491f-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a491f-349">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a491f-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a491f-350">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a491f-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a491f-351">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a491f-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-352">Az.Sql</span></span>
* <span data-ttu-id="a491f-353">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a491f-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a491f-354">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="a491f-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-355">Az.Websites</span></span>
* <span data-ttu-id="a491f-356">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a491f-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a491f-357">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a491f-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-358">Az.Accounts</span></span>
* <span data-ttu-id="a491f-359">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a491f-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a491f-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a491f-360">Az.AnalysisServices</span></span>
<span data-ttu-id="a491f-361">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a491f-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-362">Az.Compute</span></span>
* <span data-ttu-id="a491f-363">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="a491f-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a491f-364">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a491f-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a491f-365">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a491f-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-366">Az.RecoveryServices</span></span>
<span data-ttu-id="a491f-367">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a491f-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-368">Az.Resources</span></span>
* <span data-ttu-id="a491f-369">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="a491f-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a491f-370">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a491f-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a491f-371">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a491f-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a491f-372">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a491f-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-373">Az.Sql</span></span>
* <span data-ttu-id="a491f-374">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a491f-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a491f-375">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="a491f-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a491f-376">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a491f-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a491f-377">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a491f-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-378">Az.Accounts</span></span>
* <span data-ttu-id="a491f-379">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a491f-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a491f-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a491f-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="a491f-381">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a491f-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="a491f-383">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a491f-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a491f-384">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a491f-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-385">Az.Accounts</span></span>
* <span data-ttu-id="a491f-386">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a491f-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a491f-387">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a491f-388">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a491f-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a491f-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a491f-389">Az.Aks</span></span>
* <span data-ttu-id="a491f-390">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a491f-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-391">Az.Automation</span></span>
* <span data-ttu-id="a491f-392">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="a491f-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a491f-393">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a491f-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a491f-394">Az.Cdn</span></span>
* <span data-ttu-id="a491f-395">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-396">Az.Compute</span></span>
* <span data-ttu-id="a491f-397">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a491f-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a491f-398">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a491f-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a491f-399">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a491f-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a491f-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a491f-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a491f-401">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a491f-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a491f-402">Az.DataFactory</span></span>
* <span data-ttu-id="a491f-403">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a491f-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-405">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="a491f-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a491f-406">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a491f-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a491f-407">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a491f-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a491f-408">Az.IotHub</span></span>
* <span data-ttu-id="a491f-409">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a491f-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a491f-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-410">Az.KeyVault</span></span>
* <span data-ttu-id="a491f-411">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-412">Az.Network</span></span>
* <span data-ttu-id="a491f-413">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-414">Az.Resources</span></span>
* <span data-ttu-id="a491f-415">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a491f-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a491f-416">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a491f-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a491f-417">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a491f-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a491f-418">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a491f-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a491f-419">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a491f-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a491f-420">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a491f-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a491f-421">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a491f-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a491f-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a491f-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="a491f-423">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a491f-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a491f-424">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="a491f-424">Fix some error messages.</span></span>
* <span data-ttu-id="a491f-425">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a491f-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a491f-426">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="a491f-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a491f-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a491f-427">Az.SignalR</span></span>
* <span data-ttu-id="a491f-428">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-429">Az.Sql</span></span>
* <span data-ttu-id="a491f-430">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a491f-431">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="a491f-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a491f-432">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="a491f-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a491f-433">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="a491f-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a491f-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-434">Az.Storage</span></span>
* <span data-ttu-id="a491f-435">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a491f-436">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="a491f-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a491f-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a491f-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a491f-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a491f-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a491f-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a491f-439">Az.TrafficManager</span></span>
* <span data-ttu-id="a491f-440">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-441">Az.Websites</span></span>
* <span data-ttu-id="a491f-442">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="a491f-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a491f-443">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="a491f-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a491f-444">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="a491f-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a491f-445">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a491f-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-446">Az.Accounts</span></span>
* <span data-ttu-id="a491f-447">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a491f-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-448">Az.Compute</span></span>
* <span data-ttu-id="a491f-449">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a491f-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a491f-450">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="a491f-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a491f-451">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-453">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="a491f-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a491f-454">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="a491f-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a491f-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a491f-455">Az.EventGrid</span></span>
* <span data-ttu-id="a491f-456">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a491f-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a491f-457">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a491f-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a491f-458">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="a491f-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a491f-459">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="a491f-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a491f-460">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="a491f-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a491f-461">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="a491f-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a491f-462">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="a491f-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a491f-463">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="a491f-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a491f-464">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="a491f-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a491f-465">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="a491f-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="a491f-466">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a491f-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a491f-467">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a491f-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a491f-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a491f-468">Az.IotHub</span></span>
* <span data-ttu-id="a491f-469">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="a491f-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a491f-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a491f-470">Az.LogicApp</span></span>
* <span data-ttu-id="a491f-471">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="a491f-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-472">Az.Resources</span></span>
* <span data-ttu-id="a491f-473">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="a491f-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a491f-474">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a491f-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a491f-475">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a491f-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a491f-476">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a491f-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a491f-477">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="a491f-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a491f-478">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a491f-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a491f-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a491f-479">Az.SignalR</span></span>
* <span data-ttu-id="a491f-480">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-481">Az.Sql</span></span>
* <span data-ttu-id="a491f-482">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="a491f-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a491f-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-483">Az.Storage</span></span>
* <span data-ttu-id="a491f-484">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="a491f-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a491f-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a491f-485">New-AzStorageContext</span></span>
* <span data-ttu-id="a491f-486">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="a491f-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a491f-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a491f-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-488">Az.Websites</span></span>
* <span data-ttu-id="a491f-489">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="a491f-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a491f-490">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a491f-491">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a491f-492">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a491f-492">General</span></span>

- <span data-ttu-id="a491f-493">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="a491f-493">General Availability of Az Module</span></span>
- <span data-ttu-id="a491f-494">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="a491f-494">Online help for each module</span></span>
- <span data-ttu-id="a491f-495">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a491f-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a491f-496">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="a491f-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a491f-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-497">Az.Accounts</span></span>
- <span data-ttu-id="a491f-498">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a491f-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="a491f-499">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="a491f-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a491f-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a491f-500">Az.ApiManagement</span></span>
- <span data-ttu-id="a491f-501">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="a491f-501">Fixes for #7002</span></span>
- <span data-ttu-id="a491f-502">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a491f-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a491f-503">Az.Batch</span></span>
- <span data-ttu-id="a491f-504">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a491f-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a491f-505">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="a491f-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a491f-506">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a491f-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a491f-507">Az.Billing</span></span>
- <span data-ttu-id="a491f-508">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a491f-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a491f-509">Az.CognitivServices</span></span>
- <span data-ttu-id="a491f-510">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a491f-511">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a491f-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a491f-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="a491f-513">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a491f-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a491f-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a491f-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a491f-515">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a491f-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="a491f-517">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a491f-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a491f-518">Az.Monitor</span></span>
- <span data-ttu-id="a491f-519">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a491f-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a491f-520">Az.KeyVault</span></span>
- <span data-ttu-id="a491f-521">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="a491f-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a491f-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a491f-522">Az.MachineLearning</span></span>
- <span data-ttu-id="a491f-523">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a491f-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a491f-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a491f-524">Az.Media</span></span>
- <span data-ttu-id="a491f-525">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a491f-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a491f-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-526">Az.Network</span></span>
<span data-ttu-id="a491f-527">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a491f-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a491f-528">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a491f-528">New cmdlets added:</span></span>
        - <span data-ttu-id="a491f-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a491f-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a491f-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a491f-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a491f-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a491f-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a491f-537">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a491f-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a491f-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a491f-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a491f-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a491f-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a491f-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a491f-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a491f-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a491f-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a491f-543">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a491f-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a491f-544">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a491f-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a491f-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a491f-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a491f-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a491f-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a491f-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a491f-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a491f-548">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a491f-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a491f-549">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a491f-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a491f-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="a491f-551">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a491f-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a491f-552">Az.Profile</span></span>
- <span data-ttu-id="a491f-553">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a491f-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="a491f-555">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a491f-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-556">Az.Resources</span></span>
- <span data-ttu-id="a491f-557">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a491f-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a491f-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="a491f-559">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="a491f-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a491f-560">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a491f-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a491f-561">Az.SIgnalR</span></span>
- <span data-ttu-id="a491f-562">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a491f-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a491f-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-563">Az.Sql</span></span>
- <span data-ttu-id="a491f-564">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="a491f-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a491f-565">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a491f-566">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a491f-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-567">Az.Storage</span></span>
- <span data-ttu-id="a491f-568">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a491f-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-569">Az.Websites</span></span>
- <span data-ttu-id="a491f-570">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a491f-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a491f-571">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a491f-572">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a491f-572">General</span></span>

* <span data-ttu-id="a491f-573">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="a491f-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a491f-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-574">Az.Compute</span></span>

* <span data-ttu-id="a491f-575">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a491f-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a491f-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="a491f-577">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="a491f-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a491f-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a491f-578">Az.FrontDoor</span></span>

* <span data-ttu-id="a491f-579">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="a491f-579">Fixed some broken links</span></span>
    - <span data-ttu-id="a491f-580">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a491f-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a491f-581">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a491f-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a491f-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a491f-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="a491f-583">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a491f-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a491f-584">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a491f-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a491f-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-585">Az.Resources</span></span>

* <span data-ttu-id="a491f-586">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a491f-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a491f-587">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="a491f-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a491f-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-588">Az.Sql</span></span>

* <span data-ttu-id="a491f-589">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="a491f-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a491f-590">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="a491f-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a491f-591">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="a491f-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a491f-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-592">Az.Storage</span></span>

* <span data-ttu-id="a491f-593">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a491f-594">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="a491f-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a491f-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a491f-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a491f-596">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="a491f-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="a491f-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a491f-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a491f-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a491f-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a491f-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-599">Az.Websites</span></span>

* <span data-ttu-id="a491f-600">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a491f-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a491f-601">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="a491f-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a491f-602">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a491f-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a491f-603">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a491f-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a491f-604">Az.ApiManagement</span></span>
* <span data-ttu-id="a491f-605">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a491f-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a491f-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a491f-606">Az.Automation</span></span>
* <span data-ttu-id="a491f-607">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="a491f-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a491f-608">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="a491f-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a491f-609">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="a491f-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a491f-610">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a491f-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a491f-611">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="a491f-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a491f-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-612">Az.Compute</span></span>
* <span data-ttu-id="a491f-613">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a491f-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a491f-614">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a491f-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a491f-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="a491f-616">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a491f-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a491f-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a491f-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a491f-618">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="a491f-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a491f-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-619">Az.Network</span></span>
* <span data-ttu-id="a491f-620">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a491f-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a491f-621">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a491f-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a491f-622">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="a491f-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a491f-623">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a491f-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a491f-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a491f-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a491f-625">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="a491f-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a491f-626">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="a491f-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a491f-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a491f-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a491f-628">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a491f-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a491f-629">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="a491f-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a491f-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a491f-630">Az.Relay</span></span>
* <span data-ttu-id="a491f-631">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a491f-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a491f-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-632">Az.Resources</span></span>
* <span data-ttu-id="a491f-633">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a491f-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a491f-634">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="a491f-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a491f-635">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a491f-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a491f-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a491f-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="a491f-637">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="a491f-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a491f-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-638">Az.Sql</span></span>
* <span data-ttu-id="a491f-639">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a491f-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a491f-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a491f-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a491f-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a491f-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a491f-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a491f-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a491f-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a491f-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a491f-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a491f-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a491f-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a491f-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a491f-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a491f-648">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a491f-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a491f-649">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="a491f-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a491f-650">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="a491f-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a491f-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a491f-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a491f-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a491f-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a491f-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a491f-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a491f-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a491f-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a491f-655">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a491f-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a491f-656">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a491f-657">Ogólne</span><span class="sxs-lookup"><span data-stu-id="a491f-657">General</span></span>
* <span data-ttu-id="a491f-658">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="a491f-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a491f-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a491f-659">Az.Profile</span></span>
* <span data-ttu-id="a491f-660">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="a491f-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a491f-661">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="a491f-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a491f-662">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a491f-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a491f-663">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a491f-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a491f-664">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="a491f-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a491f-665">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="a491f-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a491f-666">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="a491f-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a491f-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a491f-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="a491f-668">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a491f-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-669">Az.Compute</span></span>
* <span data-ttu-id="a491f-670">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a491f-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a491f-671">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a491f-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a491f-672">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="a491f-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-674">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a491f-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a491f-675">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="a491f-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a491f-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a491f-676">Az.Insights</span></span>
* <span data-ttu-id="a491f-677">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="a491f-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a491f-678">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="a491f-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a491f-679">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="a491f-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a491f-680">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="a491f-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-681">Az.Network</span></span>
* <span data-ttu-id="a491f-682">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a491f-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a491f-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a491f-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a491f-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a491f-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a491f-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a491f-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a491f-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a491f-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a491f-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a491f-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a491f-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a491f-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a491f-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a491f-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="a491f-690">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="a491f-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-691">Az.Resources</span></span>
* <span data-ttu-id="a491f-692">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a491f-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a491f-693">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="a491f-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a491f-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a491f-694">Az.ServiceBus</span></span>
* <span data-ttu-id="a491f-695">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="a491f-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a491f-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a491f-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="a491f-697">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="a491f-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a491f-698">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="a491f-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a491f-699">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a491f-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a491f-700">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a491f-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a491f-701">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="a491f-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a491f-702">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a491f-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a491f-703">Az.Profile</span></span>
* <span data-ttu-id="a491f-704">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="a491f-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a491f-705">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="a491f-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-706">Az.Compute</span></span>
* <span data-ttu-id="a491f-707">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="a491f-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a491f-708">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a491f-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a491f-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a491f-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="a491f-710">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a491f-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a491f-711">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a491f-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a491f-712">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a491f-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a491f-713">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a491f-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a491f-714">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a491f-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-715">Az.Network</span></span>
* <span data-ttu-id="a491f-716">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a491f-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a491f-717">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a491f-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-718">Az.Resources</span></span>
* <span data-ttu-id="a491f-719">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="a491f-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a491f-720">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="a491f-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a491f-721">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a491f-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a491f-722">Azure.Storage</span></span>
* <span data-ttu-id="a491f-723">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="a491f-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a491f-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a491f-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a491f-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a491f-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a491f-726">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="a491f-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a491f-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a491f-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a491f-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a491f-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="a491f-729">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="a491f-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a491f-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a491f-730">Az.Compute</span></span>
* <span data-ttu-id="a491f-731">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="a491f-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a491f-732">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a491f-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a491f-733">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="a491f-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a491f-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a491f-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a491f-735">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a491f-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a491f-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a491f-736">Az.Network</span></span>
* <span data-ttu-id="a491f-737">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="a491f-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a491f-738">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="a491f-738">new cmdlets added</span></span>
    - <span data-ttu-id="a491f-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a491f-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a491f-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a491f-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a491f-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a491f-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a491f-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a491f-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a491f-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a491f-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a491f-745">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="a491f-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a491f-746">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a491f-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a491f-747">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a491f-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a491f-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a491f-748">Az.RedisCache</span></span>
* <span data-ttu-id="a491f-749">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="a491f-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a491f-750">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a491f-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a491f-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a491f-751">Az.Resources</span></span>
* <span data-ttu-id="a491f-752">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a491f-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a491f-753">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="a491f-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a491f-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a491f-754">Az.Sql</span></span>
* <span data-ttu-id="a491f-755">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a491f-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a491f-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a491f-756">Az.Websites</span></span>
* <span data-ttu-id="a491f-757">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="a491f-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a491f-758">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="a491f-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a491f-759">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="a491f-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a491f-760">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="a491f-760">Initial Release</span></span>