---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1cc7d6519ded41003daed558a8e78ee65ded072a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240968"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="1fcfa-103">Informacje o wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1fcfa-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="1fcfa-104">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1fcfa-105">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-105">Highlights since the last major release</span></span>
* <span data-ttu-id="1fcfa-106">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-106">General availability of `Az` module</span></span>
* <span data-ttu-id="1fcfa-107">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1fcfa-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1fcfa-108">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1fcfa-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1fcfa-109">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1fcfa-110">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1fcfa-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1fcfa-111">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1fcfa-112">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-113">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-114">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="1fcfa-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1fcfa-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1fcfa-115">Az.Batch</span></span>
* <span data-ttu-id="1fcfa-116">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1fcfa-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1fcfa-117">Az.Cdn</span></span>
* <span data-ttu-id="1fcfa-118">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1fcfa-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="1fcfa-120">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-121">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-122">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1fcfa-123">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-124">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1fcfa-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcfa-125">Az.DataFactory</span></span>
* <span data-ttu-id="1fcfa-126">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-128">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1fcfa-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1fcfa-129">Az.EventGrid</span></span>
* <span data-ttu-id="1fcfa-130">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1fcfa-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-131">Az.EventHub</span></span>
* <span data-ttu-id="1fcfa-132">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1fcfa-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1fcfa-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1fcfa-133">Az.HDInsight</span></span>
* <span data-ttu-id="1fcfa-134">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1fcfa-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-135">Az.IotHub</span></span>
* <span data-ttu-id="1fcfa-136">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1fcfa-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-137">Az.KeyVault</span></span>
* <span data-ttu-id="1fcfa-138">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-139">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1fcfa-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1fcfa-140">Az.MachineLearning</span></span>
* <span data-ttu-id="1fcfa-141">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1fcfa-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1fcfa-142">Az.Media</span></span>
* <span data-ttu-id="1fcfa-143">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1fcfa-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1fcfa-144">Az.Monitor</span></span>
  * <span data-ttu-id="1fcfa-145">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="1fcfa-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1fcfa-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1fcfa-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1fcfa-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1fcfa-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1fcfa-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1fcfa-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1fcfa-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1fcfa-151">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="1fcfa-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-152">Az.Network</span></span>
* <span data-ttu-id="1fcfa-153">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-154">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1fcfa-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1fcfa-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="1fcfa-156">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1fcfa-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1fcfa-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="1fcfa-158">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1fcfa-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1fcfa-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1fcfa-160">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="1fcfa-162">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-163">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1fcfa-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1fcfa-164">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="1fcfa-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1fcfa-165">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="1fcfa-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1fcfa-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1fcfa-166">Az.RedisCache</span></span>
* <span data-ttu-id="1fcfa-167">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-168">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-169">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-170">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-171">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="1fcfa-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1fcfa-172">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-173">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1fcfa-174">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1fcfa-175">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1fcfa-176">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1fcfa-177">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-178">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-179">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1fcfa-180">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1fcfa-181">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1fcfa-182">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1fcfa-183">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1fcfa-184">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-184">Highlights since the last major release</span></span>
* <span data-ttu-id="1fcfa-185">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-185">General availability of `Az` module</span></span>
* <span data-ttu-id="1fcfa-186">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1fcfa-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1fcfa-187">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1fcfa-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1fcfa-188">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1fcfa-189">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1fcfa-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1fcfa-190">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1fcfa-191">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-192">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-193">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1fcfa-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1fcfa-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="1fcfa-195">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1fcfa-196">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="1fcfa-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1fcfa-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-197">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-198">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1fcfa-199">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1fcfa-200">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-201">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-202">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1fcfa-203">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1fcfa-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="1fcfa-205">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="1fcfa-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1fcfa-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcfa-206">Az.DataFactory</span></span>
* <span data-ttu-id="1fcfa-207">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1fcfa-208">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-209">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-210">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1fcfa-211">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1fcfa-212">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="1fcfa-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1fcfa-213">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1fcfa-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1fcfa-214">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="1fcfa-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1fcfa-215">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1fcfa-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-216">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-217">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1fcfa-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-218">Az.Storage</span></span>
* <span data-ttu-id="1fcfa-219">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1fcfa-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1fcfa-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fcfa-220">New-AzStorageContext</span></span>
* <span data-ttu-id="1fcfa-221">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1fcfa-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1fcfa-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1fcfa-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1fcfa-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1fcfa-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1fcfa-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1fcfa-226">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="1fcfa-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1fcfa-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1fcfa-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1fcfa-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1fcfa-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1fcfa-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1fcfa-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1fcfa-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1fcfa-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1fcfa-231">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="1fcfa-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1fcfa-232">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-232">Highlights since the last major release</span></span>
* <span data-ttu-id="1fcfa-233">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-233">General availability of `Az` module</span></span>
* <span data-ttu-id="1fcfa-234">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1fcfa-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1fcfa-235">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1fcfa-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1fcfa-236">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1fcfa-237">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1fcfa-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1fcfa-238">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1fcfa-239">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1fcfa-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-240">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-241">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="1fcfa-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1fcfa-242">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="1fcfa-242">Dynamic grouping</span></span>
    * <span data-ttu-id="1fcfa-243">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-243">Pre-Post script</span></span>
    * <span data-ttu-id="1fcfa-244">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-245">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-246">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1fcfa-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1fcfa-247">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1fcfa-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-248">Az.KeyVault</span></span>
* <span data-ttu-id="1fcfa-249">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-250">Az.Network</span></span>
* <span data-ttu-id="1fcfa-251">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="1fcfa-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1fcfa-252">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="1fcfa-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="1fcfa-254">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="1fcfa-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1fcfa-255">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="1fcfa-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-256">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-257">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1fcfa-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1fcfa-258">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="1fcfa-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-259">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-260">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1fcfa-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-261">Az.Storage</span></span>
* <span data-ttu-id="1fcfa-262">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1fcfa-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1fcfa-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1fcfa-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1fcfa-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1fcfa-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1fcfa-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1fcfa-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1fcfa-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1fcfa-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-269">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-270">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="1fcfa-271">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="1fcfa-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-272">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-273">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="1fcfa-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1fcfa-274">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1fcfa-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-275">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-276">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1fcfa-277">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1fcfa-278">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="1fcfa-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1fcfa-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1fcfa-279">Az.Cdn</span></span>
* <span data-ttu-id="1fcfa-280">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="1fcfa-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-281">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-282">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1fcfa-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcfa-283">Az.DataFactory</span></span>
* <span data-ttu-id="1fcfa-284">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="1fcfa-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1fcfa-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1fcfa-285">Az.LogicApp</span></span>
* <span data-ttu-id="1fcfa-286">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="1fcfa-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-287">Az.Network</span></span>
* <span data-ttu-id="1fcfa-288">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="1fcfa-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="1fcfa-290">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1fcfa-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1fcfa-291">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="1fcfa-291">SDK Update</span></span>
* <span data-ttu-id="1fcfa-292">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1fcfa-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1fcfa-293">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1fcfa-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-294">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-295">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1fcfa-296">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="1fcfa-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1fcfa-297">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1fcfa-298">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="1fcfa-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1fcfa-299">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1fcfa-300">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="1fcfa-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-301">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-302">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1fcfa-303">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1fcfa-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-304">Az.Storage</span></span>
* <span data-ttu-id="1fcfa-305">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1fcfa-306">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1fcfa-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="1fcfa-308">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1fcfa-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-309">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-310">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1fcfa-311">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1fcfa-312">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1fcfa-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="1fcfa-314">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-315">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-316">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1fcfa-317">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="1fcfa-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1fcfa-318">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1fcfa-319">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-321">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="1fcfa-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1fcfa-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-322">Az.EventHub</span></span>
* <span data-ttu-id="1fcfa-323">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1fcfa-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-324">Az.KeyVault</span></span>
* <span data-ttu-id="1fcfa-325">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1fcfa-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1fcfa-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1fcfa-326">Az.LogicApp</span></span>
* <span data-ttu-id="1fcfa-327">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1fcfa-328">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="1fcfa-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1fcfa-329">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1fcfa-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1fcfa-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1fcfa-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1fcfa-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1fcfa-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1fcfa-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1fcfa-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1fcfa-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1fcfa-334">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1fcfa-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1fcfa-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1fcfa-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1fcfa-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1fcfa-339">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1fcfa-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1fcfa-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1fcfa-340">Az.Monitor</span></span>
* <span data-ttu-id="1fcfa-341">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="1fcfa-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-342">Az.Network</span></span>
* <span data-ttu-id="1fcfa-343">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1fcfa-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1fcfa-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1fcfa-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="1fcfa-345">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1fcfa-346">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="1fcfa-347">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-348">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-349">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1fcfa-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1fcfa-350">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1fcfa-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1fcfa-351">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="1fcfa-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1fcfa-352">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="1fcfa-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-353">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-354">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1fcfa-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1fcfa-355">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-356">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-357">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="1fcfa-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1fcfa-358">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-359">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-360">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1fcfa-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1fcfa-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-361">Az.AnalysisServices</span></span>
<span data-ttu-id="1fcfa-362">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-363">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-364">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="1fcfa-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1fcfa-365">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1fcfa-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1fcfa-366">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-367">Az.RecoveryServices</span></span>
<span data-ttu-id="1fcfa-368">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-369">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-370">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="1fcfa-371">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1fcfa-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1fcfa-372">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="1fcfa-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="1fcfa-373">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1fcfa-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-374">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-375">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1fcfa-376">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="1fcfa-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1fcfa-377">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="1fcfa-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1fcfa-378">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-379">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-380">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1fcfa-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="1fcfa-382">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="1fcfa-384">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="1fcfa-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1fcfa-385">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-386">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-387">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1fcfa-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1fcfa-388">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1fcfa-389">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="1fcfa-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1fcfa-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1fcfa-390">Az.Aks</span></span>
* <span data-ttu-id="1fcfa-391">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1fcfa-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-392">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-393">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1fcfa-394">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1fcfa-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1fcfa-395">Az.Cdn</span></span>
* <span data-ttu-id="1fcfa-396">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-397">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-398">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1fcfa-399">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1fcfa-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1fcfa-400">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1fcfa-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1fcfa-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1fcfa-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1fcfa-402">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1fcfa-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcfa-403">Az.DataFactory</span></span>
* <span data-ttu-id="1fcfa-404">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="1fcfa-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-406">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="1fcfa-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1fcfa-407">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="1fcfa-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1fcfa-408">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1fcfa-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-409">Az.IotHub</span></span>
* <span data-ttu-id="1fcfa-410">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1fcfa-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-411">Az.KeyVault</span></span>
* <span data-ttu-id="1fcfa-412">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-413">Az.Network</span></span>
* <span data-ttu-id="1fcfa-414">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-415">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-416">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1fcfa-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1fcfa-417">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1fcfa-418">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fcfa-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1fcfa-419">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="1fcfa-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1fcfa-420">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="1fcfa-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1fcfa-421">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1fcfa-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1fcfa-422">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="1fcfa-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1fcfa-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1fcfa-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="1fcfa-424">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="1fcfa-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1fcfa-425">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-425">Fix some error messages.</span></span>
* <span data-ttu-id="1fcfa-426">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1fcfa-427">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1fcfa-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1fcfa-428">Az.SignalR</span></span>
* <span data-ttu-id="1fcfa-429">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-430">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-431">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1fcfa-432">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="1fcfa-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1fcfa-433">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="1fcfa-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1fcfa-434">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="1fcfa-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1fcfa-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-435">Az.Storage</span></span>
* <span data-ttu-id="1fcfa-436">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1fcfa-437">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1fcfa-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1fcfa-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1fcfa-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1fcfa-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1fcfa-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1fcfa-440">Az.TrafficManager</span></span>
* <span data-ttu-id="1fcfa-441">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-442">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-443">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="1fcfa-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1fcfa-444">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1fcfa-445">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="1fcfa-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1fcfa-446">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1fcfa-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-447">Az.Accounts</span></span>
* <span data-ttu-id="1fcfa-448">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1fcfa-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-449">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-450">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1fcfa-451">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1fcfa-452">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-454">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1fcfa-455">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="1fcfa-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1fcfa-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1fcfa-456">Az.EventGrid</span></span>
* <span data-ttu-id="1fcfa-457">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1fcfa-458">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1fcfa-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1fcfa-459">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="1fcfa-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1fcfa-460">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="1fcfa-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1fcfa-461">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="1fcfa-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1fcfa-462">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1fcfa-463">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="1fcfa-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1fcfa-464">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="1fcfa-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1fcfa-465">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="1fcfa-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1fcfa-466">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="1fcfa-467">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1fcfa-468">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1fcfa-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-469">Az.IotHub</span></span>
* <span data-ttu-id="1fcfa-470">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="1fcfa-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1fcfa-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1fcfa-471">Az.LogicApp</span></span>
* <span data-ttu-id="1fcfa-472">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-473">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-474">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1fcfa-475">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="1fcfa-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1fcfa-476">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fcfa-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1fcfa-477">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1fcfa-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1fcfa-478">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1fcfa-479">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="1fcfa-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1fcfa-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1fcfa-480">Az.SignalR</span></span>
* <span data-ttu-id="1fcfa-481">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-482">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-483">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1fcfa-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-484">Az.Storage</span></span>
* <span data-ttu-id="1fcfa-485">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="1fcfa-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1fcfa-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fcfa-486">New-AzStorageContext</span></span>
* <span data-ttu-id="1fcfa-487">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="1fcfa-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1fcfa-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1fcfa-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-489">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-490">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1fcfa-491">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1fcfa-492">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1fcfa-493">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1fcfa-493">General</span></span>

- <span data-ttu-id="1fcfa-494">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="1fcfa-494">General Availability of Az Module</span></span>
- <span data-ttu-id="1fcfa-495">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-495">Online help for each module</span></span>
- <span data-ttu-id="1fcfa-496">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="1fcfa-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1fcfa-497">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="1fcfa-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1fcfa-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-498">Az.Accounts</span></span>
- <span data-ttu-id="1fcfa-499">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="1fcfa-500">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1fcfa-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fcfa-501">Az.ApiManagement</span></span>
- <span data-ttu-id="1fcfa-502">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="1fcfa-502">Fixes for #7002</span></span>
- <span data-ttu-id="1fcfa-503">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1fcfa-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1fcfa-504">Az.Batch</span></span>
- <span data-ttu-id="1fcfa-505">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1fcfa-506">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1fcfa-507">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1fcfa-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1fcfa-508">Az.Billing</span></span>
- <span data-ttu-id="1fcfa-509">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1fcfa-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-510">Az.CognitivServices</span></span>
- <span data-ttu-id="1fcfa-511">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1fcfa-512">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="1fcfa-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1fcfa-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="1fcfa-514">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="1fcfa-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1fcfa-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1fcfa-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1fcfa-516">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="1fcfa-518">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1fcfa-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1fcfa-519">Az.Monitor</span></span>
- <span data-ttu-id="1fcfa-520">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1fcfa-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1fcfa-521">Az.KeyVault</span></span>
- <span data-ttu-id="1fcfa-522">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="1fcfa-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1fcfa-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1fcfa-523">Az.MachineLearning</span></span>
- <span data-ttu-id="1fcfa-524">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1fcfa-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1fcfa-525">Az.Media</span></span>
- <span data-ttu-id="1fcfa-526">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1fcfa-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1fcfa-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-527">Az.Network</span></span>
<span data-ttu-id="1fcfa-528">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1fcfa-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1fcfa-529">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1fcfa-529">New cmdlets added:</span></span>
        - <span data-ttu-id="1fcfa-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1fcfa-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1fcfa-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1fcfa-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fcfa-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1fcfa-538">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1fcfa-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fcfa-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1fcfa-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1fcfa-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1fcfa-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1fcfa-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1fcfa-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1fcfa-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1fcfa-544">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1fcfa-545">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1fcfa-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1fcfa-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcfa-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1fcfa-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcfa-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1fcfa-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fcfa-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1fcfa-549">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1fcfa-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1fcfa-550">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1fcfa-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1fcfa-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="1fcfa-552">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1fcfa-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-553">Az.Profile</span></span>
- <span data-ttu-id="1fcfa-554">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1fcfa-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="1fcfa-556">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1fcfa-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-557">Az.Resources</span></span>
- <span data-ttu-id="1fcfa-558">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1fcfa-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1fcfa-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="1fcfa-560">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="1fcfa-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1fcfa-561">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1fcfa-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1fcfa-562">Az.SIgnalR</span></span>
- <span data-ttu-id="1fcfa-563">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1fcfa-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1fcfa-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-564">Az.Sql</span></span>
- <span data-ttu-id="1fcfa-565">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="1fcfa-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1fcfa-566">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1fcfa-567">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1fcfa-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-568">Az.Storage</span></span>
- <span data-ttu-id="1fcfa-569">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1fcfa-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-570">Az.Websites</span></span>
- <span data-ttu-id="1fcfa-571">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1fcfa-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1fcfa-572">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1fcfa-573">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1fcfa-573">General</span></span>

* <span data-ttu-id="1fcfa-574">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="1fcfa-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1fcfa-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-575">Az.Compute</span></span>

* <span data-ttu-id="1fcfa-576">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="1fcfa-578">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="1fcfa-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1fcfa-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1fcfa-579">Az.FrontDoor</span></span>

* <span data-ttu-id="1fcfa-580">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="1fcfa-580">Fixed some broken links</span></span>
    - <span data-ttu-id="1fcfa-581">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1fcfa-582">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1fcfa-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="1fcfa-584">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1fcfa-585">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1fcfa-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-586">Az.Resources</span></span>

* <span data-ttu-id="1fcfa-587">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="1fcfa-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1fcfa-588">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1fcfa-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-589">Az.Sql</span></span>

* <span data-ttu-id="1fcfa-590">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="1fcfa-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1fcfa-591">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="1fcfa-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1fcfa-592">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1fcfa-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-593">Az.Storage</span></span>

* <span data-ttu-id="1fcfa-594">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1fcfa-595">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="1fcfa-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1fcfa-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1fcfa-597">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="1fcfa-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1fcfa-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1fcfa-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1fcfa-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1fcfa-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-600">Az.Websites</span></span>

* <span data-ttu-id="1fcfa-601">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1fcfa-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="1fcfa-602">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1fcfa-603">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1fcfa-604">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1fcfa-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fcfa-605">Az.ApiManagement</span></span>
* <span data-ttu-id="1fcfa-606">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1fcfa-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1fcfa-607">Az.Automation</span></span>
* <span data-ttu-id="1fcfa-608">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="1fcfa-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1fcfa-609">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="1fcfa-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1fcfa-610">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="1fcfa-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1fcfa-611">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1fcfa-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1fcfa-612">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="1fcfa-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1fcfa-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-613">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-614">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="1fcfa-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1fcfa-615">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1fcfa-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="1fcfa-617">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1fcfa-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1fcfa-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1fcfa-619">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="1fcfa-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1fcfa-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-620">Az.Network</span></span>
* <span data-ttu-id="1fcfa-621">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1fcfa-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1fcfa-622">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1fcfa-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1fcfa-623">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="1fcfa-624">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1fcfa-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1fcfa-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1fcfa-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1fcfa-626">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1fcfa-627">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1fcfa-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1fcfa-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1fcfa-629">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1fcfa-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1fcfa-630">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="1fcfa-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1fcfa-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1fcfa-631">Az.Relay</span></span>
* <span data-ttu-id="1fcfa-632">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1fcfa-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-633">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-634">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="1fcfa-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1fcfa-635">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="1fcfa-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1fcfa-636">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1fcfa-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1fcfa-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1fcfa-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="1fcfa-638">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="1fcfa-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1fcfa-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-639">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-640">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="1fcfa-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1fcfa-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1fcfa-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1fcfa-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1fcfa-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1fcfa-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1fcfa-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1fcfa-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1fcfa-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1fcfa-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1fcfa-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1fcfa-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1fcfa-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1fcfa-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1fcfa-649">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1fcfa-650">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1fcfa-651">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1fcfa-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1fcfa-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1fcfa-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1fcfa-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1fcfa-656">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1fcfa-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1fcfa-657">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1fcfa-658">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1fcfa-658">General</span></span>
* <span data-ttu-id="1fcfa-659">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1fcfa-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-660">Az.Profile</span></span>
* <span data-ttu-id="1fcfa-661">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="1fcfa-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1fcfa-662">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="1fcfa-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1fcfa-663">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1fcfa-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1fcfa-664">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1fcfa-665">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="1fcfa-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1fcfa-666">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1fcfa-667">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="1fcfa-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1fcfa-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="1fcfa-669">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-670">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-671">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1fcfa-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1fcfa-672">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="1fcfa-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1fcfa-673">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-675">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1fcfa-676">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1fcfa-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1fcfa-677">Az.Insights</span></span>
* <span data-ttu-id="1fcfa-678">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="1fcfa-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1fcfa-679">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="1fcfa-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1fcfa-680">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="1fcfa-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1fcfa-681">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="1fcfa-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-682">Az.Network</span></span>
* <span data-ttu-id="1fcfa-683">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1fcfa-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1fcfa-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1fcfa-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1fcfa-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1fcfa-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1fcfa-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1fcfa-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1fcfa-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1fcfa-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1fcfa-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1fcfa-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1fcfa-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1fcfa-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1fcfa-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1fcfa-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="1fcfa-691">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="1fcfa-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-692">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-693">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="1fcfa-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1fcfa-694">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1fcfa-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1fcfa-695">Az.ServiceBus</span></span>
* <span data-ttu-id="1fcfa-696">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1fcfa-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1fcfa-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="1fcfa-698">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1fcfa-699">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1fcfa-700">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1fcfa-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1fcfa-701">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1fcfa-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1fcfa-702">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1fcfa-703">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1fcfa-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-704">Az.Profile</span></span>
* <span data-ttu-id="1fcfa-705">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="1fcfa-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1fcfa-706">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="1fcfa-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-707">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-708">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="1fcfa-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1fcfa-709">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1fcfa-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1fcfa-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="1fcfa-711">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1fcfa-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1fcfa-712">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1fcfa-713">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1fcfa-714">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1fcfa-715">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-716">Az.Network</span></span>
* <span data-ttu-id="1fcfa-717">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1fcfa-718">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-719">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-720">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1fcfa-721">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1fcfa-722">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1fcfa-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-723">Azure.Storage</span></span>
* <span data-ttu-id="1fcfa-724">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="1fcfa-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1fcfa-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1fcfa-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1fcfa-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1fcfa-727">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1fcfa-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1fcfa-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1fcfa-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1fcfa-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="1fcfa-730">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1fcfa-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1fcfa-731">Az.Compute</span></span>
* <span data-ttu-id="1fcfa-732">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="1fcfa-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1fcfa-733">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1fcfa-734">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="1fcfa-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1fcfa-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1fcfa-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1fcfa-736">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1fcfa-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1fcfa-737">Az.Network</span></span>
* <span data-ttu-id="1fcfa-738">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1fcfa-739">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="1fcfa-739">new cmdlets added</span></span>
    - <span data-ttu-id="1fcfa-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1fcfa-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1fcfa-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1fcfa-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1fcfa-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1fcfa-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1fcfa-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1fcfa-746">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="1fcfa-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1fcfa-747">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1fcfa-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1fcfa-748">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1fcfa-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1fcfa-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1fcfa-749">Az.RedisCache</span></span>
* <span data-ttu-id="1fcfa-750">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1fcfa-751">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="1fcfa-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1fcfa-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1fcfa-752">Az.Resources</span></span>
* <span data-ttu-id="1fcfa-753">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fcfa-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1fcfa-754">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="1fcfa-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1fcfa-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1fcfa-755">Az.Sql</span></span>
* <span data-ttu-id="1fcfa-756">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1fcfa-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1fcfa-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1fcfa-757">Az.Websites</span></span>
* <span data-ttu-id="1fcfa-758">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="1fcfa-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1fcfa-759">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1fcfa-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1fcfa-760">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1fcfa-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1fcfa-761">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="1fcfa-761">Initial Release</span></span>
