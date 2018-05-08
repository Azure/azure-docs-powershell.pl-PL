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
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2017
---
# <a name="release-notes"></a><span data-ttu-id="deb72-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="deb72-103">Release notes</span></span>

<span data-ttu-id="deb72-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="deb72-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="deb72-105">Wersja 1.7.0</span><span class="sxs-lookup"><span data-stu-id="deb72-105">Version 1.7.0</span></span>

* <span data-ttu-id="deb72-106">**Zmiana działania parametrów -Force, -Confirm i $ConfirmPreference dla wszystkich poleceń cmdlet. Zmieniamy tę implementację, aby była zgodna z wytycznymi programu PowerShell. W przypadku większości poleceń cmdlet oznacza to usunięcie parametru Force, zaś aby pominąć monit ShouldProcess, użytkownicy będą musieli dodać parametr: „-Confirm:$false” w swoich skryptach programu PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="deb72-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="deb72-107">Te zmiany rozwiązują następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="deb72-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="deb72-108">Poprawnej implementacji funkcjonalności -WhatIf, pozwalając użytkownikom na ustalenie efektów polecenia cmdlet lub skryptu bez wprowadzania żadnych rzeczywistych zmian</span><span class="sxs-lookup"><span data-stu-id="deb72-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="deb72-109">Kontroli nad monitowaniem przy użyciu obejmującego całą sesję parametru $ConfirmPreference, dzięki czemu użytkownik jest monitowany na podstawie wpływu potencjalnej zmiany (zgłoszonej w ustawieniu ConfirmImpact w poleceniu cmdlet)</span><span class="sxs-lookup"><span data-stu-id="deb72-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="deb72-110">Specyficznej dla polecenia cmdlet kontroli nad monitami o potwierdzenie przy użyciu parametru –Confirm</span><span class="sxs-lookup"><span data-stu-id="deb72-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="deb72-111">Spójnego używania parametru ShouldContinue i -Force w poleceniach cmdlet tylko dla tych akcji, które wymagałyby monitowania użytkownika z powodu specjalnego rodzaju zmian (na przykład usuwania plików ukrytych)</span><span class="sxs-lookup"><span data-stu-id="deb72-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="deb72-112">Spójności z innymi poleceniami cmdlet programu PowerShell, dzięki czemu wiedza o pisaniu skryptów programu PowerShell z innych poleceń cmdlet natychmiast jest stosowana do poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="deb72-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="deb72-113">**Pamiętaj, że teraz, aby *automatycznie pominąć wszystkie monity w każdych okolicznościach*, polecenia cmdlet programu Azure PowerShell wymagają podania przez użytkownika dwóch parametrów:**</span><span class="sxs-lookup"><span data-stu-id="deb72-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="deb72-114">Azure Compute</span><span class="sxs-lookup"><span data-stu-id="deb72-114">Azure Compute</span></span>
  - <span data-ttu-id="deb72-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="deb72-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="deb72-117">Parametr -Redeploy dla polecenia Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="deb72-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="deb72-118">Parametr -Validate dla poleceń Move-AzureService, Move-AzureStorageAccount i Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="deb72-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="deb72-119">Nazwa i wersja parametrów poleceń cmdlet rozszerzenia są opcjonalne jak przedtem.</span><span class="sxs-lookup"><span data-stu-id="deb72-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="deb72-120">Polecenie New-AzureVM może uzyskać typ licencji z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="deb72-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="deb72-121">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="deb72-121">Azure Storage</span></span>
  - <span data-ttu-id="deb72-122">Zmieniono parametr Tags na Tag oraz dodano alias parametru Tags</span><span class="sxs-lookup"><span data-stu-id="deb72-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="deb72-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="deb72-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="deb72-125">Azure Network</span><span class="sxs-lookup"><span data-stu-id="deb72-125">Azure Network</span></span>
  - <span data-ttu-id="deb72-126">Dodano nowe polecenie cmdlet dla równorzędnych sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="deb72-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="deb72-127">Azure Redis Cache</span><span class="sxs-lookup"><span data-stu-id="deb72-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="deb72-128">Dodano nowe polecenie cmdlet dla polecenia Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="deb72-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="deb72-129">Dodano nowe polecenie cmdlet dla polecenia Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="deb72-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="deb72-130">Dodano nowe polecenie cmdlet dla polecenia Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="deb72-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="deb72-131">Zmodyfikowano polecenie cmdlet New-AzureRmRedisCache, aby uwzględnić zmianę parametru dla sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="deb72-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="deb72-132">Przywracanie/tworzenie kopii zapasowej bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="deb72-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="deb72-133">Polecenia cmdlet dla funkcji kopii zapasowej dla długiego okresu przechowywania</span><span class="sxs-lookup"><span data-stu-id="deb72-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="deb72-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="deb72-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="deb72-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="deb72-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="deb72-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="deb72-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="deb72-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="deb72-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="deb72-138">Polecenie Restore-AzureRmSqlDatabase obsługuje teraz przywracanie do określonego momentu usuniętej bazy danych</span><span class="sxs-lookup"><span data-stu-id="deb72-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="deb72-139">Polecenie Restore-AzureRmSqlDatabase obsługuje teraz przywracanie z kopii zapasowej dla długiego okresu przechowywania</span><span class="sxs-lookup"><span data-stu-id="deb72-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="deb72-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="deb72-140">Azure LogicApp</span></span>
  - <span data-ttu-id="deb72-141">Dodano polecenia cmdlet kont integracji programu LogicApp.</span><span class="sxs-lookup"><span data-stu-id="deb72-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="deb72-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="deb72-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="deb72-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="deb72-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="deb72-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="deb72-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="deb72-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="deb72-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="deb72-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="deb72-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="deb72-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="deb72-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="deb72-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="deb72-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="deb72-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="deb72-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="deb72-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="deb72-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="deb72-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="deb72-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="deb72-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="deb72-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="deb72-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="deb72-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="deb72-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="deb72-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="deb72-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="deb72-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="deb72-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="deb72-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="deb72-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="deb72-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="deb72-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="deb72-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="deb72-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="deb72-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="deb72-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="deb72-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="deb72-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="deb72-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="deb72-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="deb72-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="deb72-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="deb72-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="deb72-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="deb72-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="deb72-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="deb72-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="deb72-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="deb72-168">Znacząco zwiększono wydajność przekazywania i pobierania plików oraz folderów.</span><span class="sxs-lookup"><span data-stu-id="deb72-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="deb72-169">Obejmuje to niewielkie zmiany nazw parametrów dla pobierania i włączenie dwóch nowych parametrów dla przekazywania:</span><span class="sxs-lookup"><span data-stu-id="deb72-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="deb72-170">NumThreads -> PerFileThreadCount, który służy do wskazywania liczby wątków do użycia w jednym pliku</span><span class="sxs-lookup"><span data-stu-id="deb72-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="deb72-171">ConcurrentFileCount, który służy do wskazywania liczby plików do równoległego przekazania/pobrania dla przekazywania/pobierania folderu.</span><span class="sxs-lookup"><span data-stu-id="deb72-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="deb72-172">Domyślne wartości wątkowości służą obecnie do zapewnienia lepszej ogólnej przepływności dla większości rozmiarów plików.</span><span class="sxs-lookup"><span data-stu-id="deb72-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="deb72-173">Jeśli wydajność nie jest taka, jak wymagana, powyższe wartości można modyfikować, aby spełnić wymagania.</span><span class="sxs-lookup"><span data-stu-id="deb72-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="deb72-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="deb72-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="deb72-175">Polecenie Get-AzureRMDataLakeAnalyticsDataSource teraz zwraca wszystkie źródła danych, gdy zostanie wywołane bez argumentów.</span><span class="sxs-lookup"><span data-stu-id="deb72-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="deb72-176">Ta zmiana spowoduje również usunięcie parametru typu źródła danych z polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb72-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="deb72-177">Ta zmiana powoduje zwracanie nowego obiektu dla operacji listy z następującymi właściwościami:</span><span class="sxs-lookup"><span data-stu-id="deb72-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="deb72-178">Type, typ źródła danych</span><span class="sxs-lookup"><span data-stu-id="deb72-178">Type, the type of data source</span></span>
    + <span data-ttu-id="deb72-179">Name, nazwa źródła danych</span><span class="sxs-lookup"><span data-stu-id="deb72-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="deb72-180">IsDefault, ma wartość true, jeśli jest to domyślne źródło danych dla konta</span><span class="sxs-lookup"><span data-stu-id="deb72-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="deb72-181">Polecenie Get-AzureRMDataLakeAnalyticsJob jest stałe dla pewnych wartości przesunięcia daty i godziny podczas filtrowania według parametru submittedBefore i submittedAfter.</span><span class="sxs-lookup"><span data-stu-id="deb72-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="deb72-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="deb72-182">Web Apps</span></span>
  - <span data-ttu-id="deb72-183">Dodano polecenie cmdlet Swap-AzureRmWebAppSlot dla zwykłej wymiany i wymiany z podglądem</span><span class="sxs-lookup"><span data-stu-id="deb72-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="deb72-184">Rozszerzono polecenie cmdlet Set-AzureRmWebAppSlot w celu obsługi wymiany automatycznej</span><span class="sxs-lookup"><span data-stu-id="deb72-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="deb72-185">Usługa Azure API Management</span><span class="sxs-lookup"><span data-stu-id="deb72-185">Azure API Management</span></span>
  - <span data-ttu-id="deb72-186">Poprawiono polecenia cmdlet wdrażania usługi Azure API Management dla polecenia AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="deb72-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="deb72-187">Usunięto polecenie cmdlet Set-AzureRmApiManagementTenantGitAccess, ponieważ właściwość Git Access jest domyślnie włączona.</span><span class="sxs-lookup"><span data-stu-id="deb72-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="deb72-188">Tworzenie kopii zapasowej usług Azure Recovery Services</span><span class="sxs-lookup"><span data-stu-id="deb72-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="deb72-189">Dodano obsługę obciążenia Azure SQL</span><span class="sxs-lookup"><span data-stu-id="deb72-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="deb72-190">Dodano obsługę tworzenia kopii zapasowych i przywracania zaszyfrowanych maszyn wirtualnych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="deb72-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="deb72-191">Backup-AzureRmRecoveryServicesBackupItem — dodano opcjonalny czas przechowywania punktów odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="deb72-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="deb72-192">Poprawiono niewielkie błędy związane z filtrem w poleceniach cmdlet Get-AzureRmRecoveryServicesBackupContainer i Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="deb72-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="deb72-193">Azure Automation</span><span class="sxs-lookup"><span data-stu-id="deb72-193">Azure Automation</span></span>
  - <span data-ttu-id="deb72-194">Dodano polecenie Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="deb72-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
