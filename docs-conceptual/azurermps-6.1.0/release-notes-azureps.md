---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461899"
---
# <a name="release-notes"></a><span data-ttu-id="41efa-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="41efa-103">Release notes</span></span>

<span data-ttu-id="41efa-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="41efa-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="41efa-105">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="41efa-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="41efa-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="41efa-106">AzureRM.Profile</span></span>
* <span data-ttu-id="41efa-107">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="41efa-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="41efa-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="41efa-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="41efa-109">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="41efa-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="41efa-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41efa-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="41efa-111">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="41efa-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="41efa-112">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41efa-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="41efa-113">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="41efa-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="41efa-114">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="41efa-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="41efa-115">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="41efa-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="41efa-116">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="41efa-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="41efa-117">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="41efa-117">Added support for MSI identity</span></span>
* <span data-ttu-id="41efa-118">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="41efa-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="41efa-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="41efa-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="41efa-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="41efa-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="41efa-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="41efa-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="41efa-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="41efa-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="41efa-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="41efa-123">AzureRM.Batch</span></span>
* <span data-ttu-id="41efa-124">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="41efa-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="41efa-125">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="41efa-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="41efa-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="41efa-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="41efa-127">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="41efa-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="41efa-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41efa-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="41efa-129">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="41efa-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="41efa-130">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="41efa-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="41efa-131">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="41efa-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="41efa-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="41efa-132">AzureRM.Network</span></span>
* <span data-ttu-id="41efa-133">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="41efa-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="41efa-134">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="41efa-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="41efa-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="41efa-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="41efa-136">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="41efa-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="41efa-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="41efa-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="41efa-138">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="41efa-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="41efa-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="41efa-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="41efa-140">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="41efa-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="41efa-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="41efa-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="41efa-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41efa-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="41efa-143">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="41efa-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="41efa-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="41efa-144">AzureRM.Sql</span></span>
* <span data-ttu-id="41efa-145">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="41efa-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="41efa-146">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="41efa-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="41efa-147">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="41efa-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="41efa-148">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="41efa-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="41efa-149">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="41efa-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="41efa-150">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41efa-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="41efa-151">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="41efa-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="41efa-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="41efa-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="41efa-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="41efa-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="41efa-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41efa-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="41efa-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="41efa-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="41efa-156">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="41efa-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>