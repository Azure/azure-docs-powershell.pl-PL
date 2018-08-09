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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653495"
---
# <a name="release-notes"></a><span data-ttu-id="6a4c9-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-103">Release notes</span></span>

<span data-ttu-id="6a4c9-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="6a4c9-105">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6a4c9-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6a4c9-106">General</span></span>
* <span data-ttu-id="6a4c9-107">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-108">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-109">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="6a4c9-110">Domyślnie wartość to zawsze true, a poszczególne zasoby mogą przesłaniać wartość domyślną.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="6a4c9-111">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6a4c9-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-112">Azure.Storage</span></span>
* <span data-ttu-id="6a4c9-113">Obsługa uzyskiwania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="6a4c9-114">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6a4c9-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a4c9-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6a4c9-116">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6a4c9-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6a4c9-117">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="6a4c9-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6a4c9-118">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6a4c9-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6a4c9-119">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6a4c9-120">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6a4c9-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6a4c9-121">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="6a4c9-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a4c9-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-122">AzureRM.Compute</span></span>
* <span data-ttu-id="6a4c9-123">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6a4c9-124">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6a4c9-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6a4c9-125">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6a4c9-126">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="6a4c9-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6a4c9-127">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6a4c9-128">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6a4c9-129">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6a4c9-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6a4c9-130">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6a4c9-131">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6a4c9-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6a4c9-132">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6a4c9-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6a4c9-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6a4c9-134">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6a4c9-135">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6a4c9-136">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6a4c9-137">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6a4c9-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a4c9-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6a4c9-139">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="6a4c9-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6a4c9-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a4c9-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="6a4c9-141">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6a4c9-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6a4c9-142">AzureRM.Insights</span></span>
* <span data-ttu-id="6a4c9-143">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6a4c9-144">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="6a4c9-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6a4c9-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a4c9-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a4c9-146">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6a4c9-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a4c9-147">AzureRM.Network</span></span>
* <span data-ttu-id="6a4c9-148">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6a4c9-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6a4c9-149">AzureRM.Resources</span></span>
* <span data-ttu-id="6a4c9-150">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6a4c9-151">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6a4c9-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a4c9-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6a4c9-153">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6a4c9-154">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="6a4c9-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6a4c9-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-155">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-156">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6a4c9-157">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6a4c9-158">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6a4c9-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6a4c9-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6a4c9-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6a4c9-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6a4c9-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6a4c9-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6a4c9-162">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6a4c9-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6a4c9-163">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6a4c9-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6a4c9-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-164">AzureRM.Storage</span></span>
* <span data-ttu-id="6a4c9-165">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="6a4c9-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6a4c9-166">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="6a4c9-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6a4c9-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a4c9-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6a4c9-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a4c9-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6a4c9-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a4c9-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6a4c9-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6a4c9-170">AzureRM.Tags</span></span>
* <span data-ttu-id="6a4c9-171">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="6a4c9-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6a4c9-172">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-173">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-174">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6a4c9-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-175">Azure.Storage</span></span>
* <span data-ttu-id="6a4c9-176">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6a4c9-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6a4c9-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6a4c9-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6a4c9-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6a4c9-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a4c9-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6a4c9-180">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6a4c9-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6a4c9-181">AzureRM.Automation</span></span>
* <span data-ttu-id="6a4c9-182">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a4c9-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-183">AzureRM.Compute</span></span>
* <span data-ttu-id="6a4c9-184">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6a4c9-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6a4c9-185">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6a4c9-186">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6a4c9-187">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6a4c9-188">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6a4c9-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a4c9-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="6a4c9-190">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6a4c9-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a4c9-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a4c9-192">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6a4c9-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6a4c9-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6a4c9-194">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6a4c9-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6a4c9-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a4c9-195">AzureRM.Network</span></span>
* <span data-ttu-id="6a4c9-196">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6a4c9-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6a4c9-197">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6a4c9-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6a4c9-198">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="6a4c9-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6a4c9-199">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6a4c9-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6a4c9-200">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6a4c9-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6a4c9-201">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="6a4c9-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6a4c9-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6a4c9-202">AzureRM.Relay</span></span>
* <span data-ttu-id="6a4c9-203">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="6a4c9-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6a4c9-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6a4c9-204">AzureRM.Resources</span></span>
* <span data-ttu-id="6a4c9-205">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6a4c9-206">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6a4c9-207">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6a4c9-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6a4c9-208">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6a4c9-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6a4c9-209">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="6a4c9-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6a4c9-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a4c9-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6a4c9-211">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6a4c9-212">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6a4c9-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6a4c9-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6a4c9-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6a4c9-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6a4c9-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6a4c9-218">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6a4c9-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a4c9-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6a4c9-220">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a4c9-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-221">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-222">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="6a4c9-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6a4c9-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6a4c9-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6a4c9-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6a4c9-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6a4c9-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6a4c9-225">AzureRM.Websites</span></span>
* <span data-ttu-id="6a4c9-226">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6a4c9-227">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="6a4c9-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6a4c9-228">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="6a4c9-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6a4c9-229">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6a4c9-230">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6a4c9-230">General</span></span>
* <span data-ttu-id="6a4c9-231">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="6a4c9-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-232">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-233">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="6a4c9-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a4c9-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-234">AzureRM.Compute</span></span>
* <span data-ttu-id="6a4c9-235">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6a4c9-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6a4c9-236">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6a4c9-237">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6a4c9-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6a4c9-238">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6a4c9-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6a4c9-239">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6a4c9-240">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6a4c9-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6a4c9-241">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6a4c9-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6a4c9-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6a4c9-243">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6a4c9-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6a4c9-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6a4c9-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6a4c9-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6a4c9-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6a4c9-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6a4c9-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a4c9-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6a4c9-248">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6a4c9-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6a4c9-249">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6a4c9-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6a4c9-250">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="6a4c9-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6a4c9-251">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="6a4c9-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6a4c9-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a4c9-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="6a4c9-253">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6a4c9-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6a4c9-254">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6a4c9-255">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6a4c9-256">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6a4c9-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a4c9-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a4c9-258">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6a4c9-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6a4c9-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a4c9-259">AzureRM.Network</span></span>
* <span data-ttu-id="6a4c9-260">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6a4c9-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6a4c9-261">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6a4c9-262">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c9-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6a4c9-263">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c9-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6a4c9-264">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6a4c9-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6a4c9-265">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6a4c9-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6a4c9-266">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6a4c9-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6a4c9-267">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6a4c9-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6a4c9-268">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a4c9-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6a4c9-269">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6a4c9-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6a4c9-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6a4c9-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6a4c9-271">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6a4c9-272">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6a4c9-273">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6a4c9-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6a4c9-274">AzureRM.Resources</span></span>
* <span data-ttu-id="6a4c9-275">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6a4c9-276">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6a4c9-277">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6a4c9-278">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="6a4c9-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6a4c9-279">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a4c9-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6a4c9-280">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6a4c9-281">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6a4c9-282">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6a4c9-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6a4c9-283">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6a4c9-284">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6a4c9-285">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6a4c9-286">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6a4c9-287">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6a4c9-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a4c9-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6a4c9-289">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a4c9-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-290">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-291">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6a4c9-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6a4c9-292">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="6a4c9-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6a4c9-293">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6a4c9-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-294">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-295">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="6a4c9-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6a4c9-296">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6a4c9-297">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-297">Azure.Storage</span></span>
* <span data-ttu-id="6a4c9-298">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a4c9-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-299">AzureRM.Compute</span></span>
* <span data-ttu-id="6a4c9-300">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="6a4c9-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6a4c9-301">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6a4c9-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6a4c9-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6a4c9-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6a4c9-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6a4c9-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6a4c9-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6a4c9-305">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6a4c9-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6a4c9-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6a4c9-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6a4c9-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6a4c9-310">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="6a4c9-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6a4c9-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6a4c9-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a4c9-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6a4c9-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a4c9-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6a4c9-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6a4c9-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6a4c9-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6a4c9-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a4c9-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6a4c9-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6a4c9-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6a4c9-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6a4c9-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6a4c9-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6a4c9-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6a4c9-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6a4c9-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6a4c9-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6a4c9-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6a4c9-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6a4c9-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6a4c9-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6a4c9-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6a4c9-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6a4c9-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6a4c9-326">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6a4c9-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a4c9-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a4c9-328">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6a4c9-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6a4c9-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6a4c9-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6a4c9-330">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="6a4c9-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6a4c9-331">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="6a4c9-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6a4c9-332">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6a4c9-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6a4c9-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6a4c9-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6a4c9-334">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6a4c9-335">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a4c9-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-336">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-337">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6a4c9-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6a4c9-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a4c9-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6a4c9-339">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6a4c9-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6a4c9-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6a4c9-340">AzureRM.Websites</span></span>
* <span data-ttu-id="6a4c9-341">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6a4c9-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6a4c9-342">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="6a4c9-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6a4c9-343">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6a4c9-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6a4c9-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6a4c9-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6a4c9-345">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="6a4c9-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6a4c9-346">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6a4c9-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-347">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-348">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a4c9-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-349">AzureRM.Compute</span></span>
* <span data-ttu-id="6a4c9-350">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="6a4c9-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6a4c9-351">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6a4c9-352">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6a4c9-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6a4c9-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6a4c9-354">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6a4c9-355">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="6a4c9-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6a4c9-356">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="6a4c9-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6a4c9-357">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="6a4c9-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6a4c9-358">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="6a4c9-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6a4c9-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a4c9-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a4c9-360">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="6a4c9-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6a4c9-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a4c9-361">AzureRM.Network</span></span>
* <span data-ttu-id="6a4c9-362">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="6a4c9-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6a4c9-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6a4c9-363">AzureRM.Resources</span></span>
* <span data-ttu-id="6a4c9-364">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6a4c9-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6a4c9-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6a4c9-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6a4c9-366">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="6a4c9-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6a4c9-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-367">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-368">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="6a4c9-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6a4c9-369">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a4c9-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6a4c9-370">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6a4c9-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6a4c9-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6a4c9-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a4c9-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6a4c9-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a4c9-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6a4c9-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6a4c9-374">AzureRM.Websites</span></span>
* <span data-ttu-id="6a4c9-375">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6a4c9-376">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a4c9-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a4c9-377">AzureRM.Profile</span></span>
* <span data-ttu-id="6a4c9-378">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="6a4c9-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6a4c9-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a4c9-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6a4c9-380">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6a4c9-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a4c9-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6a4c9-382">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6a4c9-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6a4c9-383">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a4c9-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6a4c9-384">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="6a4c9-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6a4c9-385">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="6a4c9-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6a4c9-386">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="6a4c9-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6a4c9-387">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6a4c9-388">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="6a4c9-388">Added support for MSI identity</span></span>
* <span data-ttu-id="6a4c9-389">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6a4c9-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6a4c9-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6a4c9-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6a4c9-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6a4c9-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6a4c9-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6a4c9-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6a4c9-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6a4c9-394">AzureRM.Batch</span></span>
* <span data-ttu-id="6a4c9-395">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6a4c9-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6a4c9-396">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6a4c9-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6a4c9-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6a4c9-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="6a4c9-398">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="6a4c9-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6a4c9-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a4c9-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6a4c9-400">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6a4c9-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6a4c9-401">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6a4c9-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6a4c9-402">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6a4c9-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6a4c9-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a4c9-403">AzureRM.Network</span></span>
* <span data-ttu-id="6a4c9-404">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6a4c9-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6a4c9-405">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6a4c9-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a4c9-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6a4c9-407">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6a4c9-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a4c9-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a4c9-409">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6a4c9-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6a4c9-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a4c9-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a4c9-411">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="6a4c9-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6a4c9-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a4c9-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6a4c9-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a4c9-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6a4c9-414">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="6a4c9-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a4c9-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a4c9-415">AzureRM.Sql</span></span>
* <span data-ttu-id="6a4c9-416">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="6a4c9-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6a4c9-417">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6a4c9-418">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6a4c9-419">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6a4c9-420">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="6a4c9-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6a4c9-421">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a4c9-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6a4c9-422">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6a4c9-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6a4c9-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a4c9-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6a4c9-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a4c9-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6a4c9-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a4c9-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6a4c9-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a4c9-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6a4c9-427">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="6a4c9-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>