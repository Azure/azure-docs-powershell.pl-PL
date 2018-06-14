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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853461"
---
# <a name="release-notes"></a><span data-ttu-id="3d319-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="3d319-103">Release notes</span></span>

<span data-ttu-id="3d319-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="3d319-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="3d319-105">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="3d319-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d319-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d319-106">AzureRM.Profile</span></span>
* <span data-ttu-id="3d319-107">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="3d319-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d319-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d319-108">AzureRM.Compute</span></span>
* <span data-ttu-id="3d319-109">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="3d319-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="3d319-110">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="3d319-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="3d319-111">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d319-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d319-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d319-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d319-113">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="3d319-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="3d319-114">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="3d319-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="3d319-115">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="3d319-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="3d319-116">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="3d319-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="3d319-117">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="3d319-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="3d319-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d319-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d319-119">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="3d319-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="3d319-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d319-120">AzureRM.Network</span></span>
* <span data-ttu-id="3d319-121">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="3d319-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d319-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d319-122">AzureRM.Resources</span></span>
* <span data-ttu-id="3d319-123">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="3d319-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3d319-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3d319-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3d319-125">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="3d319-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="3d319-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d319-126">AzureRM.Sql</span></span>
* <span data-ttu-id="3d319-127">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="3d319-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="3d319-128">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d319-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d319-129">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d319-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d319-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d319-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d319-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d319-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d319-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d319-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d319-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d319-133">AzureRM.Websites</span></span>
* <span data-ttu-id="3d319-134">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="3d319-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="3d319-135">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="3d319-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d319-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d319-136">AzureRM.Profile</span></span>
* <span data-ttu-id="3d319-137">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="3d319-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d319-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d319-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d319-139">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="3d319-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d319-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d319-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d319-141">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3d319-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="3d319-142">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d319-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="3d319-143">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="3d319-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="3d319-144">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="3d319-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="3d319-145">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="3d319-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="3d319-146">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="3d319-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="3d319-147">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="3d319-147">Added support for MSI identity</span></span>
* <span data-ttu-id="3d319-148">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="3d319-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="3d319-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3d319-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="3d319-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d319-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="3d319-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3d319-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="3d319-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3d319-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3d319-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3d319-153">AzureRM.Batch</span></span>
* <span data-ttu-id="3d319-154">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="3d319-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="3d319-155">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="3d319-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3d319-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3d319-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="3d319-157">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="3d319-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d319-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d319-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d319-159">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="3d319-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3d319-160">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d319-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="3d319-161">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d319-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="3d319-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d319-162">AzureRM.Network</span></span>
* <span data-ttu-id="3d319-163">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="3d319-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="3d319-164">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="3d319-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="3d319-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d319-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="3d319-166">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3d319-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="3d319-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d319-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d319-168">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3d319-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="3d319-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d319-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d319-170">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="3d319-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="3d319-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d319-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d319-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d319-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d319-173">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="3d319-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d319-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d319-174">AzureRM.Sql</span></span>
* <span data-ttu-id="3d319-175">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3d319-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="3d319-176">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="3d319-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="3d319-177">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="3d319-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="3d319-178">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="3d319-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="3d319-179">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="3d319-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="3d319-180">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d319-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d319-181">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d319-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d319-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d319-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d319-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d319-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d319-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d319-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d319-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d319-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d319-186">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="3d319-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>