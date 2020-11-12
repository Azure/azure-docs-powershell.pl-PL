---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 7d468fb760f9be23e8b8eea7f74adc1dd137e469
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408330"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e1ac3-103">Informacje o wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1ac3-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="e1ac3-104">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e1ac3-105">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-105">Highlights since the last major release</span></span>
* <span data-ttu-id="e1ac3-106">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-106">General availability of `Az` module</span></span>
* <span data-ttu-id="e1ac3-107">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e1ac3-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e1ac3-108">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e1ac3-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e1ac3-109">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e1ac3-110">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e1ac3-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e1ac3-111">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e1ac3-112">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-113">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-114">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="e1ac3-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e1ac3-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e1ac3-115">Az.Batch</span></span>
* <span data-ttu-id="e1ac3-116">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e1ac3-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e1ac3-117">Az.Cdn</span></span>
* <span data-ttu-id="e1ac3-118">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e1ac3-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1ac3-120">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-121">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-122">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e1ac3-123">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-124">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e1ac3-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e1ac3-125">Az.DataFactory</span></span>
* <span data-ttu-id="e1ac3-126">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-128">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e1ac3-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e1ac3-129">Az.EventGrid</span></span>
* <span data-ttu-id="e1ac3-130">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e1ac3-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-131">Az.EventHub</span></span>
* <span data-ttu-id="e1ac3-132">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="e1ac3-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e1ac3-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e1ac3-133">Az.HDInsight</span></span>
* <span data-ttu-id="e1ac3-134">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e1ac3-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-135">Az.IotHub</span></span>
* <span data-ttu-id="e1ac3-136">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e1ac3-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-137">Az.KeyVault</span></span>
* <span data-ttu-id="e1ac3-138">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-139">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e1ac3-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e1ac3-140">Az.MachineLearning</span></span>
* <span data-ttu-id="e1ac3-141">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e1ac3-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e1ac3-142">Az.Media</span></span>
* <span data-ttu-id="e1ac3-143">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e1ac3-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e1ac3-144">Az.Monitor</span></span>
  * <span data-ttu-id="e1ac3-145">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="e1ac3-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e1ac3-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e1ac3-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e1ac3-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e1ac3-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e1ac3-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e1ac3-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e1ac3-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e1ac3-151">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e1ac3-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-152">Az.Network</span></span>
* <span data-ttu-id="e1ac3-153">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-154">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e1ac3-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e1ac3-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="e1ac3-156">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e1ac3-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e1ac3-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="e1ac3-158">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e1ac3-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e1ac3-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e1ac3-160">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="e1ac3-162">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-163">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e1ac3-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e1ac3-164">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e1ac3-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e1ac3-165">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="e1ac3-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e1ac3-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e1ac3-166">Az.RedisCache</span></span>
* <span data-ttu-id="e1ac3-167">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-168">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-169">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-170">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-171">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="e1ac3-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e1ac3-172">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-173">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e1ac3-174">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e1ac3-175">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e1ac3-176">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e1ac3-177">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-178">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-179">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e1ac3-180">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e1ac3-181">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e1ac3-182">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e1ac3-183">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e1ac3-184">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-184">Highlights since the last major release</span></span>
* <span data-ttu-id="e1ac3-185">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-185">General availability of `Az` module</span></span>
* <span data-ttu-id="e1ac3-186">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e1ac3-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e1ac3-187">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e1ac3-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e1ac3-188">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e1ac3-189">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e1ac3-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e1ac3-190">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e1ac3-191">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-192">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-193">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e1ac3-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e1ac3-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="e1ac3-195">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e1ac3-196">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="e1ac3-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e1ac3-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-197">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-198">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e1ac3-199">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e1ac3-200">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-201">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-202">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e1ac3-203">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e1ac3-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="e1ac3-205">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="e1ac3-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e1ac3-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e1ac3-206">Az.DataFactory</span></span>
* <span data-ttu-id="e1ac3-207">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e1ac3-208">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-209">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-210">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e1ac3-211">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e1ac3-212">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="e1ac3-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e1ac3-213">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e1ac3-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e1ac3-214">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="e1ac3-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e1ac3-215">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e1ac3-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-216">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-217">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e1ac3-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-218">Az.Storage</span></span>
* <span data-ttu-id="e1ac3-219">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e1ac3-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e1ac3-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ac3-220">New-AzStorageContext</span></span>
* <span data-ttu-id="e1ac3-221">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e1ac3-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e1ac3-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e1ac3-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e1ac3-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e1ac3-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e1ac3-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e1ac3-226">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="e1ac3-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e1ac3-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e1ac3-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e1ac3-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e1ac3-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e1ac3-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e1ac3-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e1ac3-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e1ac3-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e1ac3-231">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="e1ac3-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e1ac3-232">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-232">Highlights since the last major release</span></span>
* <span data-ttu-id="e1ac3-233">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-233">General availability of `Az` module</span></span>
* <span data-ttu-id="e1ac3-234">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e1ac3-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e1ac3-235">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e1ac3-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e1ac3-236">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e1ac3-237">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e1ac3-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e1ac3-238">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e1ac3-239">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e1ac3-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-240">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-241">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="e1ac3-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e1ac3-242">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="e1ac3-242">Dynamic grouping</span></span>
    * <span data-ttu-id="e1ac3-243">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-243">Pre-Post script</span></span>
    * <span data-ttu-id="e1ac3-244">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-245">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-246">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e1ac3-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e1ac3-247">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e1ac3-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-248">Az.KeyVault</span></span>
* <span data-ttu-id="e1ac3-249">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-250">Az.Network</span></span>
* <span data-ttu-id="e1ac3-251">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="e1ac3-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e1ac3-252">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="e1ac3-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="e1ac3-254">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="e1ac3-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e1ac3-255">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="e1ac3-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-256">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-257">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1ac3-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e1ac3-258">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="e1ac3-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-259">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-260">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e1ac3-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-261">Az.Storage</span></span>
* <span data-ttu-id="e1ac3-262">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e1ac3-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e1ac3-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e1ac3-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e1ac3-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e1ac3-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e1ac3-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e1ac3-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e1ac3-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e1ac3-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-269">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-270">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="e1ac3-271">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="e1ac3-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-272">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-273">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="e1ac3-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e1ac3-274">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e1ac3-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-275">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-276">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e1ac3-277">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e1ac3-278">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="e1ac3-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e1ac3-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e1ac3-279">Az.Cdn</span></span>
* <span data-ttu-id="e1ac3-280">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="e1ac3-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-281">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-282">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e1ac3-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e1ac3-283">Az.DataFactory</span></span>
* <span data-ttu-id="e1ac3-284">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e1ac3-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e1ac3-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ac3-285">Az.LogicApp</span></span>
* <span data-ttu-id="e1ac3-286">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="e1ac3-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-287">Az.Network</span></span>
* <span data-ttu-id="e1ac3-288">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="e1ac3-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="e1ac3-290">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e1ac3-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e1ac3-291">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="e1ac3-291">SDK Update</span></span>
* <span data-ttu-id="e1ac3-292">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e1ac3-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e1ac3-293">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e1ac3-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-294">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-295">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e1ac3-296">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e1ac3-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e1ac3-297">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e1ac3-298">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e1ac3-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e1ac3-299">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e1ac3-300">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e1ac3-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-301">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-302">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e1ac3-303">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e1ac3-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-304">Az.Storage</span></span>
* <span data-ttu-id="e1ac3-305">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e1ac3-306">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e1ac3-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="e1ac3-308">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e1ac3-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-309">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-310">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e1ac3-311">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e1ac3-312">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e1ac3-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1ac3-314">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-315">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-316">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e1ac3-317">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="e1ac3-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e1ac3-318">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e1ac3-319">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-321">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="e1ac3-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e1ac3-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-322">Az.EventHub</span></span>
* <span data-ttu-id="e1ac3-323">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e1ac3-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-324">Az.KeyVault</span></span>
* <span data-ttu-id="e1ac3-325">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1ac3-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e1ac3-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ac3-326">Az.LogicApp</span></span>
* <span data-ttu-id="e1ac3-327">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e1ac3-328">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="e1ac3-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e1ac3-329">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e1ac3-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e1ac3-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e1ac3-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e1ac3-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e1ac3-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e1ac3-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e1ac3-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e1ac3-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e1ac3-334">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e1ac3-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e1ac3-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e1ac3-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e1ac3-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e1ac3-339">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e1ac3-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e1ac3-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e1ac3-340">Az.Monitor</span></span>
* <span data-ttu-id="e1ac3-341">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="e1ac3-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-342">Az.Network</span></span>
* <span data-ttu-id="e1ac3-343">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1ac3-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e1ac3-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e1ac3-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="e1ac3-345">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e1ac3-346">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="e1ac3-347">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-348">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-349">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e1ac3-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e1ac3-350">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e1ac3-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e1ac3-351">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e1ac3-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e1ac3-352">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e1ac3-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-353">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-354">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e1ac3-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e1ac3-355">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-356">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-357">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e1ac3-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e1ac3-358">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-359">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-360">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e1ac3-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e1ac3-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-361">Az.AnalysisServices</span></span>
<span data-ttu-id="e1ac3-362">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-363">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-364">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="e1ac3-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e1ac3-365">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e1ac3-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e1ac3-366">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-367">Az.RecoveryServices</span></span>
<span data-ttu-id="e1ac3-368">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-369">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-370">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="e1ac3-371">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e1ac3-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e1ac3-372">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e1ac3-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="e1ac3-373">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e1ac3-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-374">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-375">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e1ac3-376">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="e1ac3-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e1ac3-377">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e1ac3-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e1ac3-378">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-379">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-380">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e1ac3-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="e1ac3-382">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="e1ac3-384">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="e1ac3-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e1ac3-385">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-386">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-387">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e1ac3-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e1ac3-388">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e1ac3-389">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e1ac3-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e1ac3-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e1ac3-390">Az.Aks</span></span>
* <span data-ttu-id="e1ac3-391">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e1ac3-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-392">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-393">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e1ac3-394">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e1ac3-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e1ac3-395">Az.Cdn</span></span>
* <span data-ttu-id="e1ac3-396">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-397">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-398">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e1ac3-399">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e1ac3-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e1ac3-400">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e1ac3-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e1ac3-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e1ac3-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e1ac3-402">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e1ac3-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e1ac3-403">Az.DataFactory</span></span>
* <span data-ttu-id="e1ac3-404">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e1ac3-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-406">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="e1ac3-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e1ac3-407">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e1ac3-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e1ac3-408">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e1ac3-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-409">Az.IotHub</span></span>
* <span data-ttu-id="e1ac3-410">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e1ac3-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-411">Az.KeyVault</span></span>
* <span data-ttu-id="e1ac3-412">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-413">Az.Network</span></span>
* <span data-ttu-id="e1ac3-414">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-415">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-416">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e1ac3-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e1ac3-417">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e1ac3-418">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1ac3-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e1ac3-419">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e1ac3-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e1ac3-420">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e1ac3-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e1ac3-421">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ac3-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e1ac3-422">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e1ac3-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e1ac3-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1ac3-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="e1ac3-424">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e1ac3-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e1ac3-425">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-425">Fix some error messages.</span></span>
* <span data-ttu-id="e1ac3-426">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e1ac3-427">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e1ac3-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e1ac3-428">Az.SignalR</span></span>
* <span data-ttu-id="e1ac3-429">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-430">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-431">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e1ac3-432">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="e1ac3-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e1ac3-433">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="e1ac3-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e1ac3-434">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="e1ac3-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e1ac3-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-435">Az.Storage</span></span>
* <span data-ttu-id="e1ac3-436">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e1ac3-437">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e1ac3-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e1ac3-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e1ac3-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e1ac3-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e1ac3-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e1ac3-440">Az.TrafficManager</span></span>
* <span data-ttu-id="e1ac3-441">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-442">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-443">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="e1ac3-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e1ac3-444">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e1ac3-445">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="e1ac3-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e1ac3-446">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e1ac3-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-447">Az.Accounts</span></span>
* <span data-ttu-id="e1ac3-448">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e1ac3-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-449">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-450">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e1ac3-451">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e1ac3-452">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-454">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e1ac3-455">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="e1ac3-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e1ac3-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e1ac3-456">Az.EventGrid</span></span>
* <span data-ttu-id="e1ac3-457">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e1ac3-458">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e1ac3-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e1ac3-459">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="e1ac3-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e1ac3-460">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="e1ac3-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e1ac3-461">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="e1ac3-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e1ac3-462">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e1ac3-463">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="e1ac3-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e1ac3-464">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="e1ac3-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e1ac3-465">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="e1ac3-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e1ac3-466">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="e1ac3-467">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e1ac3-468">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e1ac3-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-469">Az.IotHub</span></span>
* <span data-ttu-id="e1ac3-470">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ac3-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e1ac3-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ac3-471">Az.LogicApp</span></span>
* <span data-ttu-id="e1ac3-472">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-473">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-474">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e1ac3-475">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e1ac3-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e1ac3-476">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1ac3-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e1ac3-477">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ac3-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e1ac3-478">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e1ac3-479">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e1ac3-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e1ac3-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e1ac3-480">Az.SignalR</span></span>
* <span data-ttu-id="e1ac3-481">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-482">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-483">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e1ac3-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-484">Az.Storage</span></span>
* <span data-ttu-id="e1ac3-485">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="e1ac3-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e1ac3-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ac3-486">New-AzStorageContext</span></span>
* <span data-ttu-id="e1ac3-487">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="e1ac3-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e1ac3-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e1ac3-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-489">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-490">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e1ac3-491">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e1ac3-492">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e1ac3-493">Ogólne</span><span class="sxs-lookup"><span data-stu-id="e1ac3-493">General</span></span>

- <span data-ttu-id="e1ac3-494">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="e1ac3-494">General Availability of Az Module</span></span>
- <span data-ttu-id="e1ac3-495">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-495">Online help for each module</span></span>
- <span data-ttu-id="e1ac3-496">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e1ac3-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e1ac3-497">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="e1ac3-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e1ac3-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-498">Az.Accounts</span></span>
- <span data-ttu-id="e1ac3-499">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="e1ac3-500">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e1ac3-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e1ac3-501">Az.ApiManagement</span></span>
- <span data-ttu-id="e1ac3-502">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="e1ac3-502">Fixes for #7002</span></span>
- <span data-ttu-id="e1ac3-503">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e1ac3-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e1ac3-504">Az.Batch</span></span>
- <span data-ttu-id="e1ac3-505">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e1ac3-506">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e1ac3-507">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e1ac3-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e1ac3-508">Az.Billing</span></span>
- <span data-ttu-id="e1ac3-509">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e1ac3-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-510">Az.CognitivServices</span></span>
- <span data-ttu-id="e1ac3-511">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e1ac3-512">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e1ac3-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e1ac3-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="e1ac3-514">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e1ac3-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e1ac3-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e1ac3-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e1ac3-516">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="e1ac3-518">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e1ac3-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e1ac3-519">Az.Monitor</span></span>
- <span data-ttu-id="e1ac3-520">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e1ac3-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1ac3-521">Az.KeyVault</span></span>
- <span data-ttu-id="e1ac3-522">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="e1ac3-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e1ac3-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e1ac3-523">Az.MachineLearning</span></span>
- <span data-ttu-id="e1ac3-524">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e1ac3-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e1ac3-525">Az.Media</span></span>
- <span data-ttu-id="e1ac3-526">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e1ac3-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e1ac3-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-527">Az.Network</span></span>
<span data-ttu-id="e1ac3-528">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e1ac3-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e1ac3-529">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e1ac3-529">New cmdlets added:</span></span>
        - <span data-ttu-id="e1ac3-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e1ac3-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e1ac3-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e1ac3-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1ac3-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e1ac3-538">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e1ac3-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1ac3-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e1ac3-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e1ac3-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e1ac3-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e1ac3-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e1ac3-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e1ac3-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e1ac3-544">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e1ac3-545">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1ac3-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e1ac3-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1ac3-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e1ac3-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1ac3-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e1ac3-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1ac3-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e1ac3-549">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e1ac3-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e1ac3-550">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e1ac3-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e1ac3-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="e1ac3-552">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e1ac3-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-553">Az.Profile</span></span>
- <span data-ttu-id="e1ac3-554">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1ac3-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="e1ac3-556">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e1ac3-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-557">Az.Resources</span></span>
- <span data-ttu-id="e1ac3-558">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e1ac3-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1ac3-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="e1ac3-560">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="e1ac3-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e1ac3-561">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e1ac3-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e1ac3-562">Az.SIgnalR</span></span>
- <span data-ttu-id="e1ac3-563">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e1ac3-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e1ac3-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-564">Az.Sql</span></span>
- <span data-ttu-id="e1ac3-565">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="e1ac3-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e1ac3-566">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e1ac3-567">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e1ac3-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-568">Az.Storage</span></span>
- <span data-ttu-id="e1ac3-569">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e1ac3-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-570">Az.Websites</span></span>
- <span data-ttu-id="e1ac3-571">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e1ac3-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e1ac3-572">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e1ac3-573">Ogólne</span><span class="sxs-lookup"><span data-stu-id="e1ac3-573">General</span></span>

* <span data-ttu-id="e1ac3-574">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="e1ac3-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e1ac3-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-575">Az.Compute</span></span>

* <span data-ttu-id="e1ac3-576">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="e1ac3-578">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="e1ac3-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e1ac3-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e1ac3-579">Az.FrontDoor</span></span>

* <span data-ttu-id="e1ac3-580">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="e1ac3-580">Fixed some broken links</span></span>
    - <span data-ttu-id="e1ac3-581">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e1ac3-582">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e1ac3-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="e1ac3-584">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e1ac3-585">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e1ac3-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-586">Az.Resources</span></span>

* <span data-ttu-id="e1ac3-587">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e1ac3-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e1ac3-588">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e1ac3-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-589">Az.Sql</span></span>

* <span data-ttu-id="e1ac3-590">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="e1ac3-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e1ac3-591">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="e1ac3-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e1ac3-592">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e1ac3-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-593">Az.Storage</span></span>

* <span data-ttu-id="e1ac3-594">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e1ac3-595">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="e1ac3-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e1ac3-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e1ac3-597">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="e1ac3-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e1ac3-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e1ac3-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e1ac3-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e1ac3-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-600">Az.Websites</span></span>

* <span data-ttu-id="e1ac3-601">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e1ac3-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="e1ac3-602">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e1ac3-603">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e1ac3-604">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e1ac3-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e1ac3-605">Az.ApiManagement</span></span>
* <span data-ttu-id="e1ac3-606">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e1ac3-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1ac3-607">Az.Automation</span></span>
* <span data-ttu-id="e1ac3-608">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="e1ac3-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e1ac3-609">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="e1ac3-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e1ac3-610">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="e1ac3-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e1ac3-611">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="e1ac3-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e1ac3-612">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="e1ac3-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e1ac3-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-613">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-614">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e1ac3-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e1ac3-615">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e1ac3-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="e1ac3-617">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e1ac3-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e1ac3-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e1ac3-619">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="e1ac3-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e1ac3-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-620">Az.Network</span></span>
* <span data-ttu-id="e1ac3-621">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e1ac3-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e1ac3-622">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e1ac3-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e1ac3-623">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="e1ac3-624">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1ac3-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e1ac3-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e1ac3-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e1ac3-626">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e1ac3-627">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e1ac3-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e1ac3-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e1ac3-629">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e1ac3-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e1ac3-630">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="e1ac3-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e1ac3-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e1ac3-631">Az.Relay</span></span>
* <span data-ttu-id="e1ac3-632">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e1ac3-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-633">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-634">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e1ac3-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e1ac3-635">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="e1ac3-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e1ac3-636">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e1ac3-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e1ac3-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1ac3-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="e1ac3-638">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="e1ac3-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e1ac3-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-639">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-640">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e1ac3-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e1ac3-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1ac3-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1ac3-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1ac3-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1ac3-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1ac3-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1ac3-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1ac3-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1ac3-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1ac3-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1ac3-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1ac3-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1ac3-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e1ac3-649">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e1ac3-650">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e1ac3-651">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e1ac3-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e1ac3-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e1ac3-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e1ac3-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e1ac3-656">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e1ac3-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e1ac3-657">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e1ac3-658">Ogólne</span><span class="sxs-lookup"><span data-stu-id="e1ac3-658">General</span></span>
* <span data-ttu-id="e1ac3-659">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e1ac3-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-660">Az.Profile</span></span>
* <span data-ttu-id="e1ac3-661">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="e1ac3-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e1ac3-662">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="e1ac3-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e1ac3-663">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e1ac3-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e1ac3-664">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e1ac3-665">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="e1ac3-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e1ac3-666">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e1ac3-667">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="e1ac3-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e1ac3-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1ac3-669">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-670">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-671">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e1ac3-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e1ac3-672">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e1ac3-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e1ac3-673">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-675">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e1ac3-676">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e1ac3-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e1ac3-677">Az.Insights</span></span>
* <span data-ttu-id="e1ac3-678">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="e1ac3-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e1ac3-679">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="e1ac3-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e1ac3-680">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="e1ac3-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e1ac3-681">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="e1ac3-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-682">Az.Network</span></span>
* <span data-ttu-id="e1ac3-683">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e1ac3-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e1ac3-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1ac3-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e1ac3-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e1ac3-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e1ac3-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e1ac3-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e1ac3-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e1ac3-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e1ac3-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1ac3-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e1ac3-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e1ac3-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e1ac3-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e1ac3-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="e1ac3-691">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="e1ac3-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-692">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-693">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e1ac3-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e1ac3-694">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e1ac3-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e1ac3-695">Az.ServiceBus</span></span>
* <span data-ttu-id="e1ac3-696">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e1ac3-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1ac3-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="e1ac3-698">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e1ac3-699">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e1ac3-700">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e1ac3-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e1ac3-701">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e1ac3-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e1ac3-702">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e1ac3-703">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e1ac3-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-704">Az.Profile</span></span>
* <span data-ttu-id="e1ac3-705">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="e1ac3-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e1ac3-706">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="e1ac3-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-707">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-708">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="e1ac3-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e1ac3-709">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1ac3-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1ac3-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1ac3-711">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e1ac3-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e1ac3-712">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e1ac3-713">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e1ac3-714">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e1ac3-715">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-716">Az.Network</span></span>
* <span data-ttu-id="e1ac3-717">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e1ac3-718">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-719">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-720">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e1ac3-721">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e1ac3-722">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e1ac3-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-723">Azure.Storage</span></span>
* <span data-ttu-id="e1ac3-724">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="e1ac3-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e1ac3-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e1ac3-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1ac3-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e1ac3-727">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e1ac3-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e1ac3-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e1ac3-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1ac3-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1ac3-730">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1ac3-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1ac3-731">Az.Compute</span></span>
* <span data-ttu-id="e1ac3-732">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="e1ac3-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e1ac3-733">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e1ac3-734">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="e1ac3-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e1ac3-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e1ac3-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e1ac3-736">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1ac3-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1ac3-737">Az.Network</span></span>
* <span data-ttu-id="e1ac3-738">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e1ac3-739">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="e1ac3-739">new cmdlets added</span></span>
    - <span data-ttu-id="e1ac3-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1ac3-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1ac3-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1ac3-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1ac3-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1ac3-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e1ac3-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e1ac3-746">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="e1ac3-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e1ac3-747">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e1ac3-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e1ac3-748">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e1ac3-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e1ac3-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e1ac3-749">Az.RedisCache</span></span>
* <span data-ttu-id="e1ac3-750">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e1ac3-751">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e1ac3-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1ac3-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1ac3-752">Az.Resources</span></span>
* <span data-ttu-id="e1ac3-753">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1ac3-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e1ac3-754">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="e1ac3-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1ac3-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1ac3-755">Az.Sql</span></span>
* <span data-ttu-id="e1ac3-756">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e1ac3-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1ac3-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1ac3-757">Az.Websites</span></span>
* <span data-ttu-id="e1ac3-758">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="e1ac3-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e1ac3-759">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="e1ac3-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e1ac3-760">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="e1ac3-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e1ac3-761">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="e1ac3-761">Initial Release</span></span>
