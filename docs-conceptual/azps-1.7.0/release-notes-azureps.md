---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364138"
---
## <a name="170---april-2019"></a><span data-ttu-id="ee736-101">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ee736-102">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="ee736-102">Highlights since the last major release</span></span>
* <span data-ttu-id="ee736-103">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="ee736-103">General availability of `Az` module</span></span>
* <span data-ttu-id="ee736-104">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ee736-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ee736-105">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ee736-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ee736-106">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ee736-107">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ee736-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ee736-108">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ee736-109">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="ee736-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ee736-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-110">Az.Accounts</span></span>
* <span data-ttu-id="ee736-111">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ee736-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ee736-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ee736-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="ee736-113">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="ee736-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ee736-114">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="ee736-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ee736-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-115">Az.Automation</span></span>
* <span data-ttu-id="ee736-116">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="ee736-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ee736-117">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="ee736-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ee736-118">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-119">Az.Compute</span></span>
* <span data-ttu-id="ee736-120">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ee736-121">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="ee736-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ee736-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="ee736-123">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="ee736-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ee736-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee736-124">Az.DataFactory</span></span>
* <span data-ttu-id="ee736-125">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ee736-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ee736-126">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ee736-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-127">Az.Resources</span></span>
* <span data-ttu-id="ee736-128">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="ee736-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ee736-129">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ee736-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ee736-130">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="ee736-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ee736-131">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ee736-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ee736-132">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="ee736-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ee736-133">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ee736-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-134">Az.Sql</span></span>
* <span data-ttu-id="ee736-135">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee736-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ee736-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-136">Az.Storage</span></span>
* <span data-ttu-id="ee736-137">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ee736-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ee736-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee736-138">New-AzStorageContext</span></span>
* <span data-ttu-id="ee736-139">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="ee736-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ee736-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ee736-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ee736-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ee736-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ee736-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ee736-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ee736-144">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="ee736-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ee736-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ee736-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ee736-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ee736-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ee736-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ee736-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ee736-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ee736-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ee736-149">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="ee736-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ee736-150">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="ee736-150">Highlights since the last major release</span></span>
* <span data-ttu-id="ee736-151">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="ee736-151">General availability of `Az` module</span></span>
* <span data-ttu-id="ee736-152">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ee736-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ee736-153">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ee736-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ee736-154">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ee736-155">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ee736-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ee736-156">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ee736-157">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="ee736-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ee736-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-158">Az.Automation</span></span>
* <span data-ttu-id="ee736-159">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="ee736-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ee736-160">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="ee736-160">Dynamic grouping</span></span>
    * <span data-ttu-id="ee736-161">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="ee736-161">Pre-Post script</span></span>
    * <span data-ttu-id="ee736-162">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="ee736-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-163">Az.Compute</span></span>
* <span data-ttu-id="ee736-164">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ee736-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ee736-165">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ee736-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ee736-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee736-166">Az.KeyVault</span></span>
* <span data-ttu-id="ee736-167">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee736-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-168">Az.Network</span></span>
* <span data-ttu-id="ee736-169">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ee736-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ee736-170">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="ee736-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="ee736-172">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="ee736-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ee736-173">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="ee736-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-174">Az.Resources</span></span>
* <span data-ttu-id="ee736-175">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee736-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ee736-176">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="ee736-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-177">Az.Sql</span></span>
* <span data-ttu-id="ee736-178">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="ee736-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ee736-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-179">Az.Storage</span></span>
* <span data-ttu-id="ee736-180">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="ee736-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ee736-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ee736-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ee736-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ee736-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ee736-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ee736-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ee736-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ee736-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ee736-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ee736-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-187">Az.Websites</span></span>
* <span data-ttu-id="ee736-188">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="ee736-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ee736-189">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="ee736-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ee736-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-190">Az.Accounts</span></span>
* <span data-ttu-id="ee736-191">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="ee736-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ee736-192">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ee736-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-193">Az.Automation</span></span>
* <span data-ttu-id="ee736-194">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ee736-195">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="ee736-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ee736-196">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="ee736-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ee736-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ee736-197">Az.Cdn</span></span>
* <span data-ttu-id="ee736-198">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="ee736-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-199">Az.Compute</span></span>
* <span data-ttu-id="ee736-200">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="ee736-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ee736-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee736-201">Az.DataFactory</span></span>
* <span data-ttu-id="ee736-202">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ee736-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ee736-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ee736-203">Az.LogicApp</span></span>
* <span data-ttu-id="ee736-204">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="ee736-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-205">Az.Network</span></span>
* <span data-ttu-id="ee736-206">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="ee736-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="ee736-208">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ee736-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ee736-209">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="ee736-209">SDK Update</span></span>
* <span data-ttu-id="ee736-210">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ee736-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ee736-211">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ee736-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-212">Az.Resources</span></span>
* <span data-ttu-id="ee736-213">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="ee736-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ee736-214">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ee736-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ee736-215">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do</span><span class="sxs-lookup"><span data-stu-id="ee736-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="ee736-216">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ee736-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ee736-217">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania</span><span class="sxs-lookup"><span data-stu-id="ee736-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="ee736-218">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ee736-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-219">Az.Sql</span></span>
* <span data-ttu-id="ee736-220">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ee736-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ee736-221">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="ee736-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ee736-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-222">Az.Storage</span></span>
* <span data-ttu-id="ee736-223">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ee736-224">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ee736-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ee736-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="ee736-226">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ee736-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-227">Az.Automation</span></span>
* <span data-ttu-id="ee736-228">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ee736-229">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ee736-230">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ee736-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ee736-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="ee736-232">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="ee736-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-233">Az.Compute</span></span>
* <span data-ttu-id="ee736-234">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="ee736-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ee736-235">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="ee736-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ee736-236">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ee736-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ee736-237">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ee736-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ee736-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="ee736-239">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="ee736-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ee736-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ee736-240">Az.EventHub</span></span>
* <span data-ttu-id="ee736-241">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="ee736-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ee736-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee736-242">Az.KeyVault</span></span>
* <span data-ttu-id="ee736-243">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ee736-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ee736-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ee736-244">Az.LogicApp</span></span>
* <span data-ttu-id="ee736-245">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="ee736-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ee736-246">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="ee736-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ee736-247">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="ee736-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ee736-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee736-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ee736-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee736-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ee736-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee736-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ee736-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee736-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ee736-252">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="ee736-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ee736-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ee736-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ee736-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ee736-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ee736-257">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ee736-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ee736-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ee736-258">Az.Monitor</span></span>
* <span data-ttu-id="ee736-259">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ee736-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-260">Az.Network</span></span>
* <span data-ttu-id="ee736-261">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ee736-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ee736-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ee736-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="ee736-263">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ee736-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ee736-264">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ee736-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ee736-265">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="ee736-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ee736-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-266">Az.Resources</span></span>
* <span data-ttu-id="ee736-267">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ee736-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ee736-268">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ee736-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ee736-269">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ee736-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ee736-270">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ee736-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-271">Az.Sql</span></span>
* <span data-ttu-id="ee736-272">Dodano obsługę warstwy bazy danych SQL w hiperskali</span><span class="sxs-lookup"><span data-stu-id="ee736-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ee736-273">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="ee736-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ee736-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-274">Az.Websites</span></span>
* <span data-ttu-id="ee736-275">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ee736-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ee736-276">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ee736-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-277">Az.Accounts</span></span>
* <span data-ttu-id="ee736-278">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ee736-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ee736-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ee736-279">Az.AnalysisServices</span></span>
<span data-ttu-id="ee736-280">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ee736-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-281">Az.Compute</span></span>
* <span data-ttu-id="ee736-282">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="ee736-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ee736-283">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ee736-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ee736-284">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ee736-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-285">Az.RecoveryServices</span></span>
<span data-ttu-id="ee736-286">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ee736-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-287">Az.Resources</span></span>
* <span data-ttu-id="ee736-288">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="ee736-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ee736-289">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ee736-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ee736-290">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ee736-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ee736-291">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ee736-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-292">Az.Sql</span></span>
* <span data-ttu-id="ee736-293">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee736-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ee736-294">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="ee736-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ee736-295">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ee736-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ee736-296">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ee736-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-297">Az.Accounts</span></span>
* <span data-ttu-id="ee736-298">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="ee736-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ee736-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ee736-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="ee736-300">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="ee736-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="ee736-302">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="ee736-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ee736-303">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ee736-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-304">Az.Accounts</span></span>
* <span data-ttu-id="ee736-305">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ee736-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ee736-306">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ee736-307">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ee736-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ee736-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ee736-308">Az.Aks</span></span>
* <span data-ttu-id="ee736-309">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ee736-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-310">Az.Automation</span></span>
* <span data-ttu-id="ee736-311">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="ee736-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ee736-312">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ee736-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ee736-313">Az.Cdn</span></span>
* <span data-ttu-id="ee736-314">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-315">Az.Compute</span></span>
* <span data-ttu-id="ee736-316">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ee736-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ee736-317">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ee736-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ee736-318">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee736-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ee736-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ee736-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ee736-320">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ee736-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee736-321">Az.DataFactory</span></span>
* <span data-ttu-id="ee736-322">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ee736-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ee736-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="ee736-324">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="ee736-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ee736-325">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ee736-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ee736-326">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ee736-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ee736-327">Az.IotHub</span></span>
* <span data-ttu-id="ee736-328">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ee736-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ee736-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee736-329">Az.KeyVault</span></span>
* <span data-ttu-id="ee736-330">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-331">Az.Network</span></span>
* <span data-ttu-id="ee736-332">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-333">Az.Resources</span></span>
* <span data-ttu-id="ee736-334">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ee736-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ee736-335">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ee736-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ee736-336">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee736-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ee736-337">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ee736-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ee736-338">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ee736-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ee736-339">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ee736-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ee736-340">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ee736-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ee736-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ee736-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="ee736-342">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ee736-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ee736-343">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="ee736-343">Fix some error messages.</span></span>
* <span data-ttu-id="ee736-344">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee736-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ee736-345">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="ee736-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ee736-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ee736-346">Az.SignalR</span></span>
* <span data-ttu-id="ee736-347">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-348">Az.Sql</span></span>
* <span data-ttu-id="ee736-349">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ee736-350">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="ee736-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ee736-351">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="ee736-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ee736-352">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="ee736-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ee736-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-353">Az.Storage</span></span>
* <span data-ttu-id="ee736-354">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ee736-355">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="ee736-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ee736-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ee736-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ee736-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ee736-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ee736-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ee736-358">Az.TrafficManager</span></span>
* <span data-ttu-id="ee736-359">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ee736-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-360">Az.Websites</span></span>
* <span data-ttu-id="ee736-361">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="ee736-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ee736-362">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="ee736-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ee736-363">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="ee736-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ee736-364">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ee736-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-365">Az.Accounts</span></span>
* <span data-ttu-id="ee736-366">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ee736-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-367">Az.Compute</span></span>
* <span data-ttu-id="ee736-368">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ee736-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ee736-369">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="ee736-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ee736-370">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ee736-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="ee736-372">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="ee736-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ee736-373">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="ee736-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ee736-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ee736-374">Az.EventGrid</span></span>
* <span data-ttu-id="ee736-375">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ee736-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ee736-376">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ee736-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ee736-377">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="ee736-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ee736-378">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="ee736-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ee736-379">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="ee736-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ee736-380">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ee736-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ee736-381">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="ee736-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ee736-382">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="ee736-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ee736-383">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="ee736-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ee736-384">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ee736-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="ee736-385">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ee736-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ee736-386">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ee736-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ee736-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ee736-387">Az.IotHub</span></span>
* <span data-ttu-id="ee736-388">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="ee736-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ee736-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ee736-389">Az.LogicApp</span></span>
* <span data-ttu-id="ee736-390">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="ee736-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-391">Az.Resources</span></span>
* <span data-ttu-id="ee736-392">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="ee736-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ee736-393">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ee736-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ee736-394">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee736-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ee736-395">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ee736-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ee736-396">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="ee736-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ee736-397">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ee736-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ee736-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ee736-398">Az.SignalR</span></span>
* <span data-ttu-id="ee736-399">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-400">Az.Sql</span></span>
* <span data-ttu-id="ee736-401">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="ee736-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ee736-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-402">Az.Storage</span></span>
* <span data-ttu-id="ee736-403">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="ee736-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ee736-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee736-404">New-AzStorageContext</span></span>
* <span data-ttu-id="ee736-405">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="ee736-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ee736-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ee736-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ee736-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-407">Az.Websites</span></span>
* <span data-ttu-id="ee736-408">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="ee736-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ee736-409">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ee736-410">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ee736-411">Ogólne</span><span class="sxs-lookup"><span data-stu-id="ee736-411">General</span></span>

- <span data-ttu-id="ee736-412">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="ee736-412">General Availability of Az Module</span></span>
- <span data-ttu-id="ee736-413">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="ee736-413">Online help for each module</span></span>
- <span data-ttu-id="ee736-414">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ee736-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ee736-415">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="ee736-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ee736-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-416">Az.Accounts</span></span>
- <span data-ttu-id="ee736-417">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ee736-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="ee736-418">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="ee736-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ee736-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee736-419">Az.ApiManagement</span></span>
- <span data-ttu-id="ee736-420">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="ee736-420">Fixes for #7002</span></span>
- <span data-ttu-id="ee736-421">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ee736-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ee736-422">Az.Batch</span></span>
- <span data-ttu-id="ee736-423">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ee736-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ee736-424">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="ee736-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ee736-425">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ee736-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ee736-426">Az.Billing</span></span>
- <span data-ttu-id="ee736-427">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ee736-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ee736-428">Az.CognitivServices</span></span>
- <span data-ttu-id="ee736-429">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ee736-430">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ee736-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ee736-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="ee736-432">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee736-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ee736-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ee736-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ee736-434">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ee736-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="ee736-436">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ee736-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ee736-437">Az.Monitor</span></span>
- <span data-ttu-id="ee736-438">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ee736-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee736-439">Az.KeyVault</span></span>
- <span data-ttu-id="ee736-440">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="ee736-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ee736-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ee736-441">Az.MachineLearning</span></span>
- <span data-ttu-id="ee736-442">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ee736-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ee736-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ee736-443">Az.Media</span></span>
- <span data-ttu-id="ee736-444">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ee736-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ee736-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-445">Az.Network</span></span>
<span data-ttu-id="ee736-446">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ee736-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ee736-447">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ee736-447">New cmdlets added:</span></span>
        - <span data-ttu-id="ee736-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ee736-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ee736-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ee736-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ee736-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee736-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ee736-456">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee736-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ee736-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee736-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ee736-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ee736-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ee736-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ee736-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ee736-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ee736-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ee736-462">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ee736-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ee736-463">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ee736-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ee736-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ee736-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ee736-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ee736-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ee736-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ee736-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ee736-467">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee736-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ee736-468">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ee736-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ee736-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="ee736-470">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ee736-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ee736-471">Az.Profile</span></span>
- <span data-ttu-id="ee736-472">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ee736-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="ee736-474">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ee736-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-475">Az.Resources</span></span>
- <span data-ttu-id="ee736-476">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ee736-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ee736-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="ee736-478">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="ee736-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ee736-479">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ee736-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ee736-480">Az.SIgnalR</span></span>
- <span data-ttu-id="ee736-481">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ee736-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ee736-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-482">Az.Sql</span></span>
- <span data-ttu-id="ee736-483">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="ee736-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ee736-484">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="ee736-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ee736-485">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ee736-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-486">Az.Storage</span></span>
- <span data-ttu-id="ee736-487">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ee736-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-488">Az.Websites</span></span>
- <span data-ttu-id="ee736-489">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="ee736-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ee736-490">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ee736-491">Ogólne</span><span class="sxs-lookup"><span data-stu-id="ee736-491">General</span></span>

* <span data-ttu-id="ee736-492">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="ee736-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ee736-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-493">Az.Compute</span></span>

* <span data-ttu-id="ee736-494">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ee736-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ee736-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="ee736-496">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="ee736-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ee736-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ee736-497">Az.FrontDoor</span></span>

* <span data-ttu-id="ee736-498">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="ee736-498">Fixed some broken links</span></span>
    - <span data-ttu-id="ee736-499">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ee736-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ee736-500">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ee736-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ee736-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ee736-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="ee736-502">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee736-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ee736-503">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee736-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ee736-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-504">Az.Resources</span></span>

* <span data-ttu-id="ee736-505">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ee736-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ee736-506">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="ee736-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ee736-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-507">Az.Sql</span></span>

* <span data-ttu-id="ee736-508">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="ee736-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ee736-509">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="ee736-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ee736-510">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="ee736-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ee736-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-511">Az.Storage</span></span>

* <span data-ttu-id="ee736-512">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ee736-513">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="ee736-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ee736-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ee736-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ee736-515">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="ee736-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="ee736-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ee736-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ee736-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ee736-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ee736-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-518">Az.Websites</span></span>

* <span data-ttu-id="ee736-519">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee736-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ee736-520">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="ee736-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ee736-521">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ee736-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ee736-522">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ee736-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee736-523">Az.ApiManagement</span></span>
* <span data-ttu-id="ee736-524">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="ee736-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ee736-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ee736-525">Az.Automation</span></span>
* <span data-ttu-id="ee736-526">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="ee736-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ee736-527">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="ee736-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ee736-528">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="ee736-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ee736-529">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ee736-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ee736-530">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="ee736-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ee736-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-531">Az.Compute</span></span>
* <span data-ttu-id="ee736-532">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ee736-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ee736-533">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="ee736-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ee736-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="ee736-535">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="ee736-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ee736-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ee736-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ee736-537">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="ee736-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ee736-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-538">Az.Network</span></span>
* <span data-ttu-id="ee736-539">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ee736-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ee736-540">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ee736-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ee736-541">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ee736-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ee736-542">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ee736-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ee736-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ee736-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ee736-544">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="ee736-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ee736-545">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="ee736-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ee736-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ee736-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ee736-547">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ee736-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ee736-548">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="ee736-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ee736-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ee736-549">Az.Relay</span></span>
* <span data-ttu-id="ee736-550">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ee736-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ee736-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-551">Az.Resources</span></span>
* <span data-ttu-id="ee736-552">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i</span><span class="sxs-lookup"><span data-stu-id="ee736-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="ee736-553">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="ee736-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ee736-554">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ee736-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ee736-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ee736-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="ee736-556">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="ee736-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ee736-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-557">Az.Sql</span></span>
* <span data-ttu-id="ee736-558">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ee736-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ee736-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ee736-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ee736-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ee736-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ee736-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ee736-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ee736-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ee736-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ee736-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ee736-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ee736-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ee736-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ee736-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ee736-567">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ee736-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ee736-568">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="ee736-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ee736-569">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="ee736-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ee736-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ee736-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ee736-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ee736-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ee736-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ee736-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ee736-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ee736-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ee736-574">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ee736-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ee736-575">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ee736-576">Ogólne</span><span class="sxs-lookup"><span data-stu-id="ee736-576">General</span></span>
* <span data-ttu-id="ee736-577">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee736-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ee736-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ee736-578">Az.Profile</span></span>
* <span data-ttu-id="ee736-579">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="ee736-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ee736-580">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="ee736-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ee736-581">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ee736-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ee736-582">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="ee736-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ee736-583">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="ee736-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ee736-584">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ee736-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ee736-585">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="ee736-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ee736-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ee736-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="ee736-587">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ee736-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-588">Az.Compute</span></span>
* <span data-ttu-id="ee736-589">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ee736-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ee736-590">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ee736-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ee736-591">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="ee736-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ee736-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="ee736-593">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ee736-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ee736-594">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="ee736-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ee736-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ee736-595">Az.Insights</span></span>
* <span data-ttu-id="ee736-596">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="ee736-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ee736-597">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="ee736-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ee736-598">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="ee736-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ee736-599">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="ee736-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-600">Az.Network</span></span>
* <span data-ttu-id="ee736-601">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ee736-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ee736-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee736-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ee736-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ee736-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ee736-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ee736-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ee736-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ee736-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ee736-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ee736-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ee736-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ee736-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ee736-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ee736-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="ee736-609">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="ee736-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-610">Az.Resources</span></span>
* <span data-ttu-id="ee736-611">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ee736-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ee736-612">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="ee736-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ee736-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ee736-613">Az.ServiceBus</span></span>
* <span data-ttu-id="ee736-614">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="ee736-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ee736-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ee736-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="ee736-616">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="ee736-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ee736-617">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="ee736-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ee736-618">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ee736-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ee736-619">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ee736-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ee736-620">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="ee736-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ee736-621">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ee736-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ee736-622">Az.Profile</span></span>
* <span data-ttu-id="ee736-623">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="ee736-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ee736-624">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="ee736-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-625">Az.Compute</span></span>
* <span data-ttu-id="ee736-626">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="ee736-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ee736-627">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee736-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ee736-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ee736-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="ee736-629">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ee736-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ee736-630">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee736-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ee736-631">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee736-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ee736-632">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee736-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ee736-633">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee736-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-634">Az.Network</span></span>
* <span data-ttu-id="ee736-635">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ee736-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ee736-636">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee736-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-637">Az.Resources</span></span>
* <span data-ttu-id="ee736-638">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="ee736-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ee736-639">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="ee736-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ee736-640">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ee736-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ee736-641">Azure.Storage</span></span>
* <span data-ttu-id="ee736-642">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="ee736-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ee736-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ee736-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ee736-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ee736-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ee736-645">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee736-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ee736-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ee736-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ee736-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ee736-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="ee736-648">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="ee736-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ee736-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ee736-649">Az.Compute</span></span>
* <span data-ttu-id="ee736-650">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="ee736-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ee736-651">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ee736-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ee736-652">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="ee736-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ee736-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ee736-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ee736-654">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ee736-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ee736-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ee736-655">Az.Network</span></span>
* <span data-ttu-id="ee736-656">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ee736-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ee736-657">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee736-657">new cmdlets added</span></span>
    - <span data-ttu-id="ee736-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ee736-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ee736-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ee736-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ee736-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ee736-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ee736-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ee736-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ee736-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ee736-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ee736-664">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="ee736-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ee736-665">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ee736-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ee736-666">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ee736-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ee736-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ee736-667">Az.RedisCache</span></span>
* <span data-ttu-id="ee736-668">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="ee736-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ee736-669">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ee736-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ee736-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ee736-670">Az.Resources</span></span>
* <span data-ttu-id="ee736-671">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee736-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ee736-672">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="ee736-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ee736-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ee736-673">Az.Sql</span></span>
* <span data-ttu-id="ee736-674">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ee736-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ee736-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ee736-675">Az.Websites</span></span>
* <span data-ttu-id="ee736-676">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="ee736-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ee736-677">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="ee736-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ee736-678">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="ee736-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ee736-679">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="ee736-679">Initial Release</span></span>