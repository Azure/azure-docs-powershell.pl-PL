---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475394"
---
## <a name="160---march-2019"></a><span data-ttu-id="840f1-101">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="840f1-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="840f1-102">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="840f1-102">Highlights since the last major release</span></span>
* <span data-ttu-id="840f1-103">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="840f1-103">General availability of `Az` module</span></span>
* <span data-ttu-id="840f1-104">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="840f1-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="840f1-105">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="840f1-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="840f1-106">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="840f1-107">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="840f1-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="840f1-108">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="840f1-109">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="840f1-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="840f1-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-110">Az.Automation</span></span>
* <span data-ttu-id="840f1-111">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="840f1-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="840f1-112">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="840f1-112">Dynamic grouping</span></span>
    * <span data-ttu-id="840f1-113">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="840f1-113">Pre-Post script</span></span>
    * <span data-ttu-id="840f1-114">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="840f1-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-115">Az.Compute</span></span>
* <span data-ttu-id="840f1-116">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="840f1-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="840f1-117">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="840f1-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="840f1-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="840f1-118">Az.KeyVault</span></span>
* <span data-ttu-id="840f1-119">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="840f1-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-120">Az.Network</span></span>
* <span data-ttu-id="840f1-121">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="840f1-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="840f1-122">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="840f1-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="840f1-124">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="840f1-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="840f1-125">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="840f1-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-126">Az.Resources</span></span>
* <span data-ttu-id="840f1-127">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="840f1-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="840f1-128">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="840f1-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-129">Az.Sql</span></span>
* <span data-ttu-id="840f1-130">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="840f1-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="840f1-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-131">Az.Storage</span></span>
* <span data-ttu-id="840f1-132">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="840f1-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="840f1-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="840f1-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="840f1-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="840f1-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="840f1-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="840f1-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="840f1-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="840f1-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="840f1-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="840f1-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="840f1-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="840f1-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="840f1-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-139">Az.Websites</span></span>
* <span data-ttu-id="840f1-140">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="840f1-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="840f1-141">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="840f1-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="840f1-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-142">Az.Accounts</span></span>
* <span data-ttu-id="840f1-143">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="840f1-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="840f1-144">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="840f1-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-145">Az.Automation</span></span>
* <span data-ttu-id="840f1-146">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="840f1-147">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="840f1-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="840f1-148">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="840f1-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="840f1-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="840f1-149">Az.Cdn</span></span>
* <span data-ttu-id="840f1-150">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="840f1-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-151">Az.Compute</span></span>
* <span data-ttu-id="840f1-152">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="840f1-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="840f1-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="840f1-153">Az.DataFactory</span></span>
* <span data-ttu-id="840f1-154">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="840f1-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="840f1-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="840f1-155">Az.LogicApp</span></span>
* <span data-ttu-id="840f1-156">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="840f1-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-157">Az.Network</span></span>
* <span data-ttu-id="840f1-158">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="840f1-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="840f1-160">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="840f1-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="840f1-161">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="840f1-161">SDK Update</span></span>
* <span data-ttu-id="840f1-162">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="840f1-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="840f1-163">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="840f1-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-164">Az.Resources</span></span>
* <span data-ttu-id="840f1-165">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="840f1-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="840f1-166">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="840f1-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="840f1-167">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="840f1-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="840f1-168">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="840f1-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="840f1-169">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="840f1-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="840f1-170">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="840f1-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-171">Az.Sql</span></span>
* <span data-ttu-id="840f1-172">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="840f1-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="840f1-173">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="840f1-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="840f1-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-174">Az.Storage</span></span>
* <span data-ttu-id="840f1-175">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="840f1-176">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="840f1-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="840f1-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="840f1-178">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="840f1-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-179">Az.Automation</span></span>
* <span data-ttu-id="840f1-180">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="840f1-181">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="840f1-182">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="840f1-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="840f1-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="840f1-184">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="840f1-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-185">Az.Compute</span></span>
* <span data-ttu-id="840f1-186">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="840f1-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="840f1-187">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="840f1-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="840f1-188">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="840f1-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="840f1-189">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="840f1-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="840f1-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="840f1-191">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="840f1-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="840f1-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="840f1-192">Az.EventHub</span></span>
* <span data-ttu-id="840f1-193">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="840f1-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="840f1-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="840f1-194">Az.KeyVault</span></span>
* <span data-ttu-id="840f1-195">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="840f1-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="840f1-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="840f1-196">Az.LogicApp</span></span>
* <span data-ttu-id="840f1-197">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="840f1-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="840f1-198">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="840f1-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="840f1-199">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="840f1-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="840f1-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="840f1-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="840f1-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="840f1-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="840f1-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="840f1-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="840f1-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="840f1-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="840f1-204">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="840f1-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="840f1-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="840f1-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="840f1-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="840f1-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="840f1-209">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="840f1-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="840f1-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="840f1-210">Az.Monitor</span></span>
* <span data-ttu-id="840f1-211">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="840f1-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-212">Az.Network</span></span>
* <span data-ttu-id="840f1-213">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="840f1-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="840f1-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="840f1-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="840f1-215">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="840f1-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="840f1-216">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="840f1-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="840f1-217">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="840f1-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="840f1-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-218">Az.Resources</span></span>
* <span data-ttu-id="840f1-219">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="840f1-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="840f1-220">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="840f1-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="840f1-221">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="840f1-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="840f1-222">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="840f1-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-223">Az.Sql</span></span>
* <span data-ttu-id="840f1-224">Dodano obsługę warstwy bazy danych SQL w hiperskali</span><span class="sxs-lookup"><span data-stu-id="840f1-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="840f1-225">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="840f1-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="840f1-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-226">Az.Websites</span></span>
* <span data-ttu-id="840f1-227">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="840f1-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="840f1-228">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="840f1-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-229">Az.Accounts</span></span>
* <span data-ttu-id="840f1-230">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="840f1-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="840f1-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="840f1-231">Az.AnalysisServices</span></span>
<span data-ttu-id="840f1-232">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="840f1-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-233">Az.Compute</span></span>
* <span data-ttu-id="840f1-234">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="840f1-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="840f1-235">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="840f1-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="840f1-236">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="840f1-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-237">Az.RecoveryServices</span></span>
<span data-ttu-id="840f1-238">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="840f1-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-239">Az.Resources</span></span>
* <span data-ttu-id="840f1-240">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="840f1-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="840f1-241">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="840f1-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="840f1-242">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="840f1-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="840f1-243">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="840f1-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-244">Az.Sql</span></span>
* <span data-ttu-id="840f1-245">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="840f1-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="840f1-246">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="840f1-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="840f1-247">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="840f1-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="840f1-248">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="840f1-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-249">Az.Accounts</span></span>
* <span data-ttu-id="840f1-250">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="840f1-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="840f1-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="840f1-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="840f1-252">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="840f1-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="840f1-254">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="840f1-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="840f1-255">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="840f1-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-256">Az.Accounts</span></span>
* <span data-ttu-id="840f1-257">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="840f1-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="840f1-258">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="840f1-259">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="840f1-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="840f1-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="840f1-260">Az.Aks</span></span>
* <span data-ttu-id="840f1-261">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="840f1-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-262">Az.Automation</span></span>
* <span data-ttu-id="840f1-263">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="840f1-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="840f1-264">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="840f1-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="840f1-265">Az.Cdn</span></span>
* <span data-ttu-id="840f1-266">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-267">Az.Compute</span></span>
* <span data-ttu-id="840f1-268">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="840f1-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="840f1-269">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="840f1-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="840f1-270">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="840f1-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="840f1-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="840f1-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="840f1-272">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="840f1-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="840f1-273">Az.DataFactory</span></span>
* <span data-ttu-id="840f1-274">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="840f1-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="840f1-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="840f1-276">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="840f1-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="840f1-277">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="840f1-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="840f1-278">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="840f1-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="840f1-279">Az.IotHub</span></span>
* <span data-ttu-id="840f1-280">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="840f1-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="840f1-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="840f1-281">Az.KeyVault</span></span>
* <span data-ttu-id="840f1-282">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-283">Az.Network</span></span>
* <span data-ttu-id="840f1-284">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-285">Az.Resources</span></span>
* <span data-ttu-id="840f1-286">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="840f1-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="840f1-287">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="840f1-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="840f1-288">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="840f1-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="840f1-289">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="840f1-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="840f1-290">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="840f1-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="840f1-291">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="840f1-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="840f1-292">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="840f1-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="840f1-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="840f1-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="840f1-294">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="840f1-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="840f1-295">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="840f1-295">Fix some error messages.</span></span>
* <span data-ttu-id="840f1-296">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="840f1-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="840f1-297">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="840f1-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="840f1-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="840f1-298">Az.SignalR</span></span>
* <span data-ttu-id="840f1-299">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-300">Az.Sql</span></span>
* <span data-ttu-id="840f1-301">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="840f1-302">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="840f1-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="840f1-303">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="840f1-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="840f1-304">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="840f1-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="840f1-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-305">Az.Storage</span></span>
* <span data-ttu-id="840f1-306">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="840f1-307">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="840f1-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="840f1-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="840f1-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="840f1-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="840f1-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="840f1-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="840f1-310">Az.TrafficManager</span></span>
* <span data-ttu-id="840f1-311">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="840f1-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-312">Az.Websites</span></span>
* <span data-ttu-id="840f1-313">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="840f1-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="840f1-314">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="840f1-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="840f1-315">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="840f1-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="840f1-316">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="840f1-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-317">Az.Accounts</span></span>
* <span data-ttu-id="840f1-318">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="840f1-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-319">Az.Compute</span></span>
* <span data-ttu-id="840f1-320">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="840f1-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="840f1-321">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="840f1-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="840f1-322">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="840f1-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="840f1-324">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="840f1-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="840f1-325">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="840f1-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="840f1-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="840f1-326">Az.EventGrid</span></span>
* <span data-ttu-id="840f1-327">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="840f1-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="840f1-328">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="840f1-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="840f1-329">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="840f1-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="840f1-330">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="840f1-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="840f1-331">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="840f1-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="840f1-332">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="840f1-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="840f1-333">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="840f1-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="840f1-334">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="840f1-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="840f1-335">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="840f1-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="840f1-336">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="840f1-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="840f1-337">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="840f1-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="840f1-338">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="840f1-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="840f1-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="840f1-339">Az.IotHub</span></span>
* <span data-ttu-id="840f1-340">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="840f1-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="840f1-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="840f1-341">Az.LogicApp</span></span>
* <span data-ttu-id="840f1-342">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="840f1-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-343">Az.Resources</span></span>
* <span data-ttu-id="840f1-344">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="840f1-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="840f1-345">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="840f1-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="840f1-346">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="840f1-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="840f1-347">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="840f1-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="840f1-348">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="840f1-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="840f1-349">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="840f1-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="840f1-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="840f1-350">Az.SignalR</span></span>
* <span data-ttu-id="840f1-351">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-352">Az.Sql</span></span>
* <span data-ttu-id="840f1-353">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="840f1-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="840f1-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-354">Az.Storage</span></span>
* <span data-ttu-id="840f1-355">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="840f1-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="840f1-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="840f1-356">New-AzStorageContext</span></span>
* <span data-ttu-id="840f1-357">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="840f1-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="840f1-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="840f1-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="840f1-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-359">Az.Websites</span></span>
* <span data-ttu-id="840f1-360">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="840f1-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="840f1-361">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="840f1-362">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="840f1-363">Ogólne</span><span class="sxs-lookup"><span data-stu-id="840f1-363">General</span></span>

- <span data-ttu-id="840f1-364">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="840f1-364">General Availability of Az Module</span></span>
- <span data-ttu-id="840f1-365">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="840f1-365">Online help for each module</span></span>
- <span data-ttu-id="840f1-366">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="840f1-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="840f1-367">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="840f1-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="840f1-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-368">Az.Accounts</span></span>
- <span data-ttu-id="840f1-369">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="840f1-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="840f1-370">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="840f1-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="840f1-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="840f1-371">Az.ApiManagement</span></span>
- <span data-ttu-id="840f1-372">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="840f1-372">Fixes for #7002</span></span>
- <span data-ttu-id="840f1-373">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="840f1-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="840f1-374">Az.Batch</span></span>
- <span data-ttu-id="840f1-375">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="840f1-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="840f1-376">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="840f1-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="840f1-377">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="840f1-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="840f1-378">Az.Billing</span></span>
- <span data-ttu-id="840f1-379">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="840f1-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="840f1-380">Az.CognitivServices</span></span>
- <span data-ttu-id="840f1-381">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="840f1-382">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="840f1-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="840f1-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="840f1-384">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="840f1-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="840f1-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="840f1-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="840f1-386">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="840f1-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="840f1-388">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="840f1-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="840f1-389">Az.Monitor</span></span>
- <span data-ttu-id="840f1-390">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="840f1-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="840f1-391">Az.KeyVault</span></span>
- <span data-ttu-id="840f1-392">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="840f1-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="840f1-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="840f1-393">Az.MachineLearning</span></span>
- <span data-ttu-id="840f1-394">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="840f1-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="840f1-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="840f1-395">Az.Media</span></span>
- <span data-ttu-id="840f1-396">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="840f1-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="840f1-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-397">Az.Network</span></span>
<span data-ttu-id="840f1-398">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="840f1-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="840f1-399">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="840f1-399">New cmdlets added:</span></span>
        - <span data-ttu-id="840f1-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="840f1-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="840f1-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="840f1-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="840f1-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="840f1-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="840f1-408">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="840f1-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="840f1-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="840f1-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="840f1-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="840f1-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="840f1-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="840f1-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="840f1-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="840f1-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="840f1-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="840f1-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="840f1-414">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="840f1-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="840f1-415">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="840f1-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="840f1-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="840f1-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="840f1-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="840f1-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="840f1-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="840f1-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="840f1-419">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="840f1-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="840f1-420">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="840f1-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="840f1-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="840f1-422">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="840f1-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="840f1-423">Az.Profile</span></span>
- <span data-ttu-id="840f1-424">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="840f1-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="840f1-426">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="840f1-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-427">Az.Resources</span></span>
- <span data-ttu-id="840f1-428">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="840f1-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="840f1-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="840f1-430">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="840f1-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="840f1-431">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="840f1-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="840f1-432">Az.SIgnalR</span></span>
- <span data-ttu-id="840f1-433">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="840f1-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="840f1-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-434">Az.Sql</span></span>
- <span data-ttu-id="840f1-435">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="840f1-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="840f1-436">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="840f1-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="840f1-437">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="840f1-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-438">Az.Storage</span></span>
- <span data-ttu-id="840f1-439">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="840f1-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-440">Az.Websites</span></span>
- <span data-ttu-id="840f1-441">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="840f1-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="840f1-442">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="840f1-443">Ogólne</span><span class="sxs-lookup"><span data-stu-id="840f1-443">General</span></span>

* <span data-ttu-id="840f1-444">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="840f1-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="840f1-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-445">Az.Compute</span></span>

* <span data-ttu-id="840f1-446">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="840f1-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="840f1-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="840f1-448">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="840f1-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="840f1-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="840f1-449">Az.FrontDoor</span></span>

* <span data-ttu-id="840f1-450">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="840f1-450">Fixed some broken links</span></span>
    - <span data-ttu-id="840f1-451">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="840f1-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="840f1-452">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="840f1-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="840f1-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="840f1-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="840f1-454">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="840f1-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="840f1-455">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="840f1-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="840f1-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-456">Az.Resources</span></span>

* <span data-ttu-id="840f1-457">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="840f1-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="840f1-458">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="840f1-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="840f1-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-459">Az.Sql</span></span>

* <span data-ttu-id="840f1-460">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="840f1-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="840f1-461">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="840f1-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="840f1-462">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="840f1-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="840f1-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-463">Az.Storage</span></span>

* <span data-ttu-id="840f1-464">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="840f1-465">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="840f1-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="840f1-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="840f1-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="840f1-467">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="840f1-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="840f1-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="840f1-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="840f1-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="840f1-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="840f1-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-470">Az.Websites</span></span>

* <span data-ttu-id="840f1-471">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="840f1-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="840f1-472">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="840f1-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="840f1-473">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="840f1-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="840f1-474">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="840f1-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="840f1-475">Az.ApiManagement</span></span>
* <span data-ttu-id="840f1-476">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="840f1-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="840f1-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="840f1-477">Az.Automation</span></span>
* <span data-ttu-id="840f1-478">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="840f1-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="840f1-479">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="840f1-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="840f1-480">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="840f1-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="840f1-481">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="840f1-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="840f1-482">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="840f1-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="840f1-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-483">Az.Compute</span></span>
* <span data-ttu-id="840f1-484">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="840f1-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="840f1-485">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="840f1-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="840f1-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="840f1-487">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="840f1-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="840f1-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="840f1-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="840f1-489">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="840f1-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="840f1-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-490">Az.Network</span></span>
* <span data-ttu-id="840f1-491">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="840f1-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="840f1-492">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="840f1-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="840f1-493">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="840f1-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="840f1-494">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="840f1-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="840f1-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="840f1-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="840f1-496">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="840f1-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="840f1-497">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="840f1-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="840f1-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="840f1-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="840f1-499">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="840f1-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="840f1-500">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="840f1-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="840f1-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="840f1-501">Az.Relay</span></span>
* <span data-ttu-id="840f1-502">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="840f1-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="840f1-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-503">Az.Resources</span></span>
* <span data-ttu-id="840f1-504">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="840f1-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="840f1-505">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="840f1-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="840f1-506">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="840f1-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="840f1-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="840f1-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="840f1-508">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="840f1-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="840f1-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-509">Az.Sql</span></span>
* <span data-ttu-id="840f1-510">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="840f1-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="840f1-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="840f1-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="840f1-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="840f1-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="840f1-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="840f1-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="840f1-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="840f1-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="840f1-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="840f1-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="840f1-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="840f1-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="840f1-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="840f1-519">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="840f1-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="840f1-520">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="840f1-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="840f1-521">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="840f1-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="840f1-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="840f1-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="840f1-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="840f1-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="840f1-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="840f1-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="840f1-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="840f1-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="840f1-526">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="840f1-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="840f1-527">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="840f1-528">Ogólne</span><span class="sxs-lookup"><span data-stu-id="840f1-528">General</span></span>
* <span data-ttu-id="840f1-529">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="840f1-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="840f1-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="840f1-530">Az.Profile</span></span>
* <span data-ttu-id="840f1-531">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="840f1-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="840f1-532">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="840f1-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="840f1-533">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="840f1-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="840f1-534">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="840f1-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="840f1-535">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="840f1-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="840f1-536">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="840f1-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="840f1-537">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="840f1-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="840f1-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="840f1-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="840f1-539">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="840f1-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-540">Az.Compute</span></span>
* <span data-ttu-id="840f1-541">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="840f1-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="840f1-542">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="840f1-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="840f1-543">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="840f1-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="840f1-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="840f1-545">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="840f1-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="840f1-546">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="840f1-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="840f1-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="840f1-547">Az.Insights</span></span>
* <span data-ttu-id="840f1-548">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="840f1-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="840f1-549">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="840f1-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="840f1-550">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="840f1-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="840f1-551">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="840f1-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-552">Az.Network</span></span>
* <span data-ttu-id="840f1-553">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="840f1-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="840f1-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="840f1-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="840f1-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="840f1-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="840f1-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="840f1-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="840f1-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="840f1-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="840f1-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="840f1-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="840f1-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="840f1-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="840f1-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="840f1-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="840f1-561">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="840f1-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-562">Az.Resources</span></span>
* <span data-ttu-id="840f1-563">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="840f1-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="840f1-564">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="840f1-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="840f1-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="840f1-565">Az.ServiceBus</span></span>
* <span data-ttu-id="840f1-566">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="840f1-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="840f1-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="840f1-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="840f1-568">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="840f1-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="840f1-569">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="840f1-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="840f1-570">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="840f1-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="840f1-571">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="840f1-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="840f1-572">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="840f1-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="840f1-573">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="840f1-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="840f1-574">Az.Profile</span></span>
* <span data-ttu-id="840f1-575">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="840f1-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="840f1-576">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="840f1-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-577">Az.Compute</span></span>
* <span data-ttu-id="840f1-578">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="840f1-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="840f1-579">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840f1-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="840f1-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="840f1-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="840f1-581">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="840f1-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="840f1-582">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="840f1-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="840f1-583">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="840f1-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="840f1-584">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="840f1-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="840f1-585">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="840f1-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-586">Az.Network</span></span>
* <span data-ttu-id="840f1-587">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="840f1-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="840f1-588">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840f1-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-589">Az.Resources</span></span>
* <span data-ttu-id="840f1-590">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="840f1-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="840f1-591">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="840f1-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="840f1-592">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="840f1-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="840f1-593">Azure.Storage</span></span>
* <span data-ttu-id="840f1-594">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="840f1-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="840f1-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="840f1-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="840f1-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="840f1-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="840f1-597">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="840f1-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="840f1-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="840f1-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="840f1-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="840f1-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="840f1-600">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="840f1-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="840f1-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="840f1-601">Az.Compute</span></span>
* <span data-ttu-id="840f1-602">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="840f1-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="840f1-603">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="840f1-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="840f1-604">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="840f1-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="840f1-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="840f1-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="840f1-606">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="840f1-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="840f1-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="840f1-607">Az.Network</span></span>
* <span data-ttu-id="840f1-608">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="840f1-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="840f1-609">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="840f1-609">new cmdlets added</span></span>
    - <span data-ttu-id="840f1-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="840f1-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="840f1-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="840f1-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="840f1-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="840f1-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="840f1-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="840f1-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="840f1-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="840f1-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="840f1-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="840f1-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="840f1-616">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="840f1-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="840f1-617">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="840f1-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="840f1-618">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="840f1-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="840f1-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="840f1-619">Az.RedisCache</span></span>
* <span data-ttu-id="840f1-620">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="840f1-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="840f1-621">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="840f1-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="840f1-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="840f1-622">Az.Resources</span></span>
* <span data-ttu-id="840f1-623">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="840f1-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="840f1-624">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="840f1-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="840f1-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="840f1-625">Az.Sql</span></span>
* <span data-ttu-id="840f1-626">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="840f1-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="840f1-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="840f1-627">Az.Websites</span></span>
* <span data-ttu-id="840f1-628">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="840f1-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="840f1-629">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="840f1-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="840f1-630">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="840f1-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="840f1-631">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="840f1-631">Initial Release</span></span>