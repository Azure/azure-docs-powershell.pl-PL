---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237817"
---
# <a name="release-notes"></a><span data-ttu-id="43a6d-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="43a6d-103">Release notes</span></span>

<span data-ttu-id="43a6d-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="43a6d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="43a6d-105">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="43a6d-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="43a6d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="43a6d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="43a6d-107">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="43a6d-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="43a6d-108">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="43a6d-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="43a6d-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="43a6d-109">Azure.Storage</span></span>
* <span data-ttu-id="43a6d-110">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="43a6d-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="43a6d-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="43a6d-111">AzureRM.Compute</span></span>
* <span data-ttu-id="43a6d-112">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="43a6d-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="43a6d-113">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="43a6d-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="43a6d-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="43a6d-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="43a6d-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="43a6d-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="43a6d-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="43a6d-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="43a6d-117">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="43a6d-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="43a6d-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="43a6d-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="43a6d-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="43a6d-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="43a6d-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="43a6d-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="43a6d-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="43a6d-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="43a6d-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="43a6d-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="43a6d-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="43a6d-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="43a6d-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="43a6d-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="43a6d-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="43a6d-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="43a6d-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="43a6d-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="43a6d-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="43a6d-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="43a6d-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="43a6d-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="43a6d-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="43a6d-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="43a6d-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="43a6d-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="43a6d-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="43a6d-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="43a6d-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="43a6d-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="43a6d-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="43a6d-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="43a6d-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="43a6d-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="43a6d-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="43a6d-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="43a6d-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="43a6d-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="43a6d-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="43a6d-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="43a6d-138">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="43a6d-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="43a6d-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43a6d-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="43a6d-140">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="43a6d-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="43a6d-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="43a6d-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="43a6d-142">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="43a6d-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="43a6d-143">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="43a6d-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="43a6d-144">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="43a6d-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="43a6d-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="43a6d-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="43a6d-146">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="43a6d-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="43a6d-147">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="43a6d-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="43a6d-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="43a6d-148">AzureRM.Sql</span></span>
* <span data-ttu-id="43a6d-149">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="43a6d-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="43a6d-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="43a6d-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="43a6d-151">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="43a6d-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="43a6d-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="43a6d-152">AzureRM.Websites</span></span>
* <span data-ttu-id="43a6d-153">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="43a6d-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="43a6d-154">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="43a6d-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="43a6d-155">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="43a6d-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="43a6d-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="43a6d-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="43a6d-157">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="43a6d-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="43a6d-158">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="43a6d-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="43a6d-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="43a6d-159">AzureRM.Profile</span></span>
* <span data-ttu-id="43a6d-160">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="43a6d-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="43a6d-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="43a6d-161">AzureRM.Compute</span></span>
* <span data-ttu-id="43a6d-162">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="43a6d-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="43a6d-163">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="43a6d-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="43a6d-164">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="43a6d-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="43a6d-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="43a6d-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="43a6d-166">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="43a6d-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="43a6d-167">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="43a6d-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="43a6d-168">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="43a6d-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="43a6d-169">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="43a6d-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="43a6d-170">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="43a6d-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="43a6d-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="43a6d-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="43a6d-172">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="43a6d-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="43a6d-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="43a6d-173">AzureRM.Network</span></span>
* <span data-ttu-id="43a6d-174">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="43a6d-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="43a6d-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="43a6d-175">AzureRM.Resources</span></span>
* <span data-ttu-id="43a6d-176">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="43a6d-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="43a6d-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="43a6d-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="43a6d-178">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="43a6d-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="43a6d-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="43a6d-179">AzureRM.Sql</span></span>
* <span data-ttu-id="43a6d-180">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="43a6d-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="43a6d-181">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43a6d-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="43a6d-182">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43a6d-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="43a6d-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="43a6d-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="43a6d-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="43a6d-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="43a6d-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43a6d-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="43a6d-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="43a6d-186">AzureRM.Websites</span></span>
* <span data-ttu-id="43a6d-187">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="43a6d-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="43a6d-188">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="43a6d-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="43a6d-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="43a6d-189">AzureRM.Profile</span></span>
* <span data-ttu-id="43a6d-190">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="43a6d-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="43a6d-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="43a6d-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="43a6d-192">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="43a6d-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="43a6d-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43a6d-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="43a6d-194">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="43a6d-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="43a6d-195">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43a6d-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="43a6d-196">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="43a6d-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="43a6d-197">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="43a6d-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="43a6d-198">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="43a6d-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="43a6d-199">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="43a6d-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="43a6d-200">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="43a6d-200">Added support for MSI identity</span></span>
* <span data-ttu-id="43a6d-201">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="43a6d-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="43a6d-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="43a6d-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="43a6d-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="43a6d-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="43a6d-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="43a6d-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="43a6d-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="43a6d-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="43a6d-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="43a6d-206">AzureRM.Batch</span></span>
* <span data-ttu-id="43a6d-207">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="43a6d-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="43a6d-208">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="43a6d-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="43a6d-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="43a6d-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="43a6d-210">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="43a6d-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="43a6d-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="43a6d-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="43a6d-212">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="43a6d-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="43a6d-213">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="43a6d-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="43a6d-214">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="43a6d-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="43a6d-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="43a6d-215">AzureRM.Network</span></span>
* <span data-ttu-id="43a6d-216">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="43a6d-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="43a6d-217">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="43a6d-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="43a6d-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="43a6d-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="43a6d-219">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="43a6d-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="43a6d-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="43a6d-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="43a6d-221">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="43a6d-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="43a6d-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="43a6d-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="43a6d-223">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="43a6d-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="43a6d-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="43a6d-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="43a6d-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="43a6d-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="43a6d-226">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="43a6d-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="43a6d-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="43a6d-227">AzureRM.Sql</span></span>
* <span data-ttu-id="43a6d-228">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="43a6d-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="43a6d-229">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="43a6d-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="43a6d-230">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="43a6d-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="43a6d-231">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="43a6d-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="43a6d-232">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="43a6d-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="43a6d-233">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43a6d-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="43a6d-234">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43a6d-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="43a6d-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="43a6d-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="43a6d-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="43a6d-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="43a6d-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43a6d-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="43a6d-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="43a6d-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="43a6d-239">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="43a6d-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>