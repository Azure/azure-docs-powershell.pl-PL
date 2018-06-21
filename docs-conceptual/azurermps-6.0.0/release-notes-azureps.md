---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912007"
---
# <a name="release-notes"></a><span data-ttu-id="b069d-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="b069d-103">Release notes</span></span>

<span data-ttu-id="b069d-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="b069d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="b069d-105">6.0.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b069d-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="b069d-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b069d-106">General</span></span>
* <span data-ttu-id="b069d-107">Ustawianie zależności minimalnej modułów na program PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="b069d-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="b069d-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b069d-108">Azure.Storage</span></span>
* <span data-ttu-id="b069d-109">Obsługa jako nazwa kontenera magazynu usługi Storage Blob</span><span class="sxs-lookup"><span data-stu-id="b069d-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="b069d-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b069d-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="b069d-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b069d-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="b069d-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b069d-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="b069d-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b069d-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="b069d-114">Rozwiązano problem polegający na tym, że niektóre dane wyjściowe dotyczące błędów nie zawierają szczegółowych informacji o błędzie</span><span class="sxs-lookup"><span data-stu-id="b069d-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="b069d-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b069d-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b069d-116">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-117">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="b069d-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b069d-118">AzureRM.Automation</span></span>
* <span data-ttu-id="b069d-119">Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b069d-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="b069d-120">„Set-AzureRmAutomationRunbook”</span><span class="sxs-lookup"><span data-stu-id="b069d-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="b069d-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b069d-121">AzureRM.Batch</span></span>
* <span data-ttu-id="b069d-122">Zaktualizowano dokumentację polecenia New-AzureBatchPool w celu usunięcia przestarzałego przykładu</span><span class="sxs-lookup"><span data-stu-id="b069d-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="b069d-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b069d-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="b069d-124">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-125">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="b069d-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b069d-126">AzureRM.Compute</span></span>
* <span data-ttu-id="b069d-127">Polecenia „New-AzureRmVm” i „New-AzureRmVmss” obsługują pełne dane wyjściowe parametrów</span><span class="sxs-lookup"><span data-stu-id="b069d-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="b069d-128">Polecenia „New-AzureRmVm” i „New-AzureRmVmss” (prosty zestaw parametrów) obsługują przypisywanie maszynom wirtualnych tożsamości zdefiniowanych przez użytkownika i/lub system.</span><span class="sxs-lookup"><span data-stu-id="b069d-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="b069d-129">Ponowne wdrażanie zestawu skalowania maszyn wirtualnych i funkcja PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="b069d-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="b069d-130">Dodano nowy parametr przełącznika -Redeploy and -PerformMaintenance do poleceń „New-AzureRmVm” i „New-AzureRmVmss”</span><span class="sxs-lookup"><span data-stu-id="b069d-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="b069d-131">Dodano parametr przełącznika DisableVMAgent do polecenia cmdlet „Set-AzureRmVMOperatingSystem”</span><span class="sxs-lookup"><span data-stu-id="b069d-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="b069d-132">Polecenia „New-AzureRmVm” i „New-AzureRmVmss” (prosty zestaw parametrów) obsługują obraz „Win10”.</span><span class="sxs-lookup"><span data-stu-id="b069d-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="b069d-133">Dodano polecenie cmdlet „Repair-AzureRmVmssServiceFabricUpdateDomain”.</span><span class="sxs-lookup"><span data-stu-id="b069d-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="b069d-134">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-135">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="b069d-136">Polecenie „Set-AzureRmVmDiskEncryptionExtension” umożliwia opcjonalne użycie parametrów usługi AAD</span><span class="sxs-lookup"><span data-stu-id="b069d-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="b069d-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="b069d-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="b069d-138">Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b069d-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="b069d-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b069d-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b069d-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b069d-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b069d-141">Zaktualizowano zestaw ADF .Net SDK do wersji 0.7.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="b069d-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b069d-142">Dodano parametry wykonywania i właściwość menedżerów połączenia w działaniu ExecuteSSISPackage</span><span class="sxs-lookup"><span data-stu-id="b069d-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="b069d-143">Zaktualizowano połączoną usługę baz danych PostgreSql i MySql w celu używania pełnych parametrów połączenia zamiast serwera, bazy danych, schematu, nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="b069d-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="b069d-144">Wyłączono schemat z połączonej usługi bazy danych DB2</span><span class="sxs-lookup"><span data-stu-id="b069d-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="b069d-145">Usunięto właściwość schematu z połączonej usługi programu Teradata</span><span class="sxs-lookup"><span data-stu-id="b069d-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="b069d-146">Dodano elementy LinkedService, Dataset i CopySource do rozwiązania Responsys</span><span class="sxs-lookup"><span data-stu-id="b069d-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b069d-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b069d-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b069d-148">Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b069d-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="b069d-149">„New-AzureRmDataLakeAnalyticsAccount”</span><span class="sxs-lookup"><span data-stu-id="b069d-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="b069d-150">„Set-AzureRmDataLakeAnalyticsAccount”</span><span class="sxs-lookup"><span data-stu-id="b069d-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="b069d-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b069d-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b069d-152">Dodano nową funkcję służącą do cyklicznej zmiany listy ACL do poleceń Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry i Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b069d-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b069d-153">Dodano nowe polecenie cmdlet służące do pobierania podsumowania zawartości w ramach katalogu</span><span class="sxs-lookup"><span data-stu-id="b069d-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="b069d-154">Dodano nowe polecenie cmdlet służące do pobierania użycia dysku i zrzutu listy ACL</span><span class="sxs-lookup"><span data-stu-id="b069d-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="b069d-155">Poprawiono typ zwracany wartości logicznej polecenia Set-AzureRmDataLakeStoreItemAcl na interfejs IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="b069d-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="b069d-156">Poprawiono typ zwracany wartości logicznej polecenia Set-AzureRmDataLakeStoreItemAclEntry na interfejs IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="b069d-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="b069d-157">Zmiany powodujące niezgodność dotyczące poleceń Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem i Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b069d-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="b069d-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b069d-158">AzureRM.Dns</span></span>
* <span data-ttu-id="b069d-159">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-160">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="b069d-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b069d-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="b069d-162">Zaktualizowano informacje pomocy dotyczącą poleceń cmdlet brakującymi przykładami</span><span class="sxs-lookup"><span data-stu-id="b069d-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="b069d-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b069d-163">AzureRM.Insights</span></span>
* <span data-ttu-id="b069d-164">Wprowadzono wiele zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-165">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="b069d-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b069d-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="b069d-167">Włączono tagi i podstawową jednostkę SKU w usłudze IotHub</span><span class="sxs-lookup"><span data-stu-id="b069d-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b069d-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b069d-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b069d-169">Zmiany powodujące niezgodność dotyczące obsługi scenariuszy z potokami</span><span class="sxs-lookup"><span data-stu-id="b069d-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="b069d-170">Dodano nowe polecenia cmdlet: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval i Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="b069d-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="b069d-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b069d-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="b069d-172">Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b069d-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="b069d-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b069d-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="b069d-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="b069d-174">AzureRM.Media</span></span>
* <span data-ttu-id="b069d-175">Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b069d-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="b069d-176">„Set-AzureRmMediaService”</span><span class="sxs-lookup"><span data-stu-id="b069d-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b069d-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b069d-177">AzureRM.Network</span></span>
* <span data-ttu-id="b069d-178">Dodano obsługę zasobów planu ochrony przed atakami DDoS</span><span class="sxs-lookup"><span data-stu-id="b069d-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="b069d-179">Wprowadzono wiele zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-180">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="b069d-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b069d-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="b069d-182">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-183">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="b069d-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b069d-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b069d-185">Wprowadzenie wielu zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-186">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="b069d-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b069d-187">AzureRM.Profile</span></span>
* <span data-ttu-id="b069d-188">Domyślnie włączono automatyczne zapisywanie kontekstu</span><span class="sxs-lookup"><span data-stu-id="b069d-188">Enable context autosave by default</span></span>
* <span data-ttu-id="b069d-189">Dodano właściwości USGovernmentOperationalInsightsEndpoint i USGovernmentOperationalInsightsEndpointResourceId do środowiska platformy Azure dla instytucji rządowych USA.</span><span class="sxs-lookup"><span data-stu-id="b069d-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b069d-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b069d-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b069d-191">Naprawiono nagłówek uwierzytelnienia w scenariuszach usługi SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b069d-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="b069d-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b069d-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b069d-193">Wprowadzono wiele zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-194">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="b069d-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b069d-195">AzureRM.Resources</span></span>
* <span data-ttu-id="b069d-196">Usunięto przestarzały parametr -AtScopeAndBelow z wywołania Get-AzureRmRoledefinition</span><span class="sxs-lookup"><span data-stu-id="b069d-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="b069d-197">Dołączono przypisania do usuniętych użytkowników/grup/jednostek usługi w wynikach polecenia Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b069d-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="b069d-198">Dodano moduły wypełniania kart dla zakresu i typu zasobu</span><span class="sxs-lookup"><span data-stu-id="b069d-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="b069d-199">Dodano wygodne polecenie cmdlet służące do tworzenia wygody tworzenia jednostek usługi</span><span class="sxs-lookup"><span data-stu-id="b069d-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="b069d-200">Scalono funkcje Get- i Find w poleceniu Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b069d-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="b069d-201">Dodawano polecenia cmdlet usługi AD:</span><span class="sxs-lookup"><span data-stu-id="b069d-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="b069d-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b069d-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="b069d-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="b069d-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="b069d-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="b069d-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="b069d-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="b069d-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="b069d-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b069d-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="b069d-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b069d-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="b069d-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b069d-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="b069d-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b069d-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="b069d-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b069d-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b069d-211">Zaktualizowano domyślną jednostkę SKU wersji obrazu systemu Linux</span><span class="sxs-lookup"><span data-stu-id="b069d-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="b069d-212">Domyślna aktualizacja jednostki SKU serwera UbuntuServer1604 (plik NewAzureServiceFabricCluster.cs)</span><span class="sxs-lookup"><span data-stu-id="b069d-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="b069d-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b069d-213">AzureRM.Storage</span></span>
* <span data-ttu-id="b069d-214">Wprowadzono wiele zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b069d-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="b069d-215">Więcej informacji można znaleźć w przewodniku po migracji</span><span class="sxs-lookup"><span data-stu-id="b069d-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="b069d-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b069d-216">AzureRM.Websites</span></span>
* <span data-ttu-id="b069d-217">Przeprowadzono uaktualnienie do najnowszej wersji zestawu SDK witryn internetowych</span><span class="sxs-lookup"><span data-stu-id="b069d-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="b069d-218">Dodane właściwości -AssignIdentity i -Httpsonly do poleceń Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b069d-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="b069d-219">Dodano dwa nowe polecenia cmdlet: Get-AzureRmWebAppSnapshots i Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b069d-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
