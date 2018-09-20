# <a name="azure-stack-module-140"></a><span data-ttu-id="c51bd-101">Moduł usługi Azure Stack w wersji 1.4.0</span><span class="sxs-lookup"><span data-stu-id="c51bd-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c51bd-102">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="c51bd-102">Requirements:</span></span>
<span data-ttu-id="c51bd-103">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="c51bd-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="c51bd-104">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="c51bd-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="c51bd-105">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="c51bd-105">Known issues:</span></span>

- <span data-ttu-id="c51bd-106">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="c51bd-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="c51bd-107">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="c51bd-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="c51bd-108">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="c51bd-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="c51bd-109">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c51bd-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="c51bd-110">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="c51bd-110">Breaking Changes</span></span>
<span data-ttu-id="c51bd-111">Nie ma zmian powodujących niezgodność względem wersji 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="c51bd-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="c51bd-112">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="c51bd-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="c51bd-113">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="c51bd-113">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="c51bd-114">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="c51bd-114">Release Notes</span></span>
    * <span data-ttu-id="c51bd-115">W wersji 1.4.0 usługi Azure Stack nie wprowadzono żadnych zmian powodujących niezgodność z poprzednią wersją, 1.3.0</span><span class="sxs-lookup"><span data-stu-id="c51bd-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="c51bd-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="c51bd-117">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="c51bd-119">Dodano nowe parametry (BackupFrequencyInHours, IsBackupSchedulerEnabled i BackupRetentionPeriodInDays) do polecenia cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="c51bd-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="c51bd-120">Dodano polecenie cmdlet New-EncyptionKeyBase64 ułatwiające tworzenie klucza szyfrowania</span><span class="sxs-lookup"><span data-stu-id="c51bd-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="c51bd-121">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="c51bd-123">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="c51bd-125">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="c51bd-126">Dodano polecenie cmdlet Add-AzsScaleUnitNode, aby umożliwić administratorowi dodawanie nowych węzłów jednostki skalowania do zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="c51bd-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="c51bd-127">Dodano polecenie cmdlet New-AzsScaleUnitNodeObject ułatwiające tworzenie obiektów parametrów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="c51bd-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="c51bd-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="c51bd-129">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="c51bd-131">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="c51bd-133">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="c51bd-135">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="c51bd-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="c51bd-137">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c51bd-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="c51bd-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="c51bd-139">Dodano polecenie cmdlet Move-AzsSubscription umożliwiające przenoszenie subskrypcji między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="c51bd-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="c51bd-140">Dodano polecenie cmdlet Test-AzsMoveSubscription służące do weryfikowania, czy subskrypcje użytkownika można przenosić między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="c51bd-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="c51bd-141">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="c51bd-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="c51bd-142">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="c51bd-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="c51bd-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="c51bd-143">Azure Bridge</span></span>
<span data-ttu-id="c51bd-144">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c51bd-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="c51bd-145">Backup</span><span class="sxs-lookup"><span data-stu-id="c51bd-145">Backup</span></span>
<span data-ttu-id="c51bd-146">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="c51bd-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="c51bd-147">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="c51bd-147">Configure where backups are stored</span></span>
- <span data-ttu-id="c51bd-148">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="c51bd-148">Perform backups</span></span>
- <span data-ttu-id="c51bd-149">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="c51bd-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="c51bd-150">Commerce</span><span class="sxs-lookup"><span data-stu-id="c51bd-150">Commerce</span></span>
<span data-ttu-id="c51bd-151">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="c51bd-152">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="c51bd-152">Compute</span></span>
<span data-ttu-id="c51bd-153">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c51bd-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="c51bd-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="c51bd-154">Fabric</span></span>
<span data-ttu-id="c51bd-155">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="c51bd-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="c51bd-156">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="c51bd-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="c51bd-157">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="c51bd-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="c51bd-158">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="c51bd-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="c51bd-159">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="c51bd-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="c51bd-160">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="c51bd-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="c51bd-161">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="c51bd-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="c51bd-162">Galeria</span><span class="sxs-lookup"><span data-stu-id="c51bd-162">Gallery</span></span>
<span data-ttu-id="c51bd-163">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="c51bd-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="c51bd-164">Infrastructure Insights</span></span>
<span data-ttu-id="c51bd-165">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="c51bd-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="c51bd-166">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="c51bd-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="c51bd-167">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="c51bd-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="c51bd-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c51bd-168">KeyVault</span></span>
<span data-ttu-id="c51bd-169">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c51bd-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="c51bd-170">Sieć</span><span class="sxs-lookup"><span data-stu-id="c51bd-170">Network</span></span>
<span data-ttu-id="c51bd-171">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="c51bd-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="c51bd-172">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="c51bd-172">Management of network quotas</span></span>
- <span data-ttu-id="c51bd-173">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c51bd-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="c51bd-174">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="c51bd-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="c51bd-175">Magazyn</span><span class="sxs-lookup"><span data-stu-id="c51bd-175">Storage</span></span>
<span data-ttu-id="c51bd-176">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="c51bd-177">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="c51bd-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="c51bd-178">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="c51bd-178">Manage storage quotas</span></span>
- <span data-ttu-id="c51bd-179">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="c51bd-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="c51bd-180">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="c51bd-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="c51bd-181">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="c51bd-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="c51bd-182">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="c51bd-182">View information about the individual storage components</span></span>
- <span data-ttu-id="c51bd-183">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="c51bd-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="c51bd-184">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="c51bd-184">Subscription Admin</span></span>
<span data-ttu-id="c51bd-185">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="c51bd-186">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="c51bd-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="c51bd-187">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="c51bd-187">Manage plans and offers</span></span>
- <span data-ttu-id="c51bd-188">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="c51bd-188">View usage and performance information</span></span>
- <span data-ttu-id="c51bd-189">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="c51bd-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="c51bd-190">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="c51bd-190">Subscription</span></span>
<span data-ttu-id="c51bd-191">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="c51bd-192">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="c51bd-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="c51bd-193">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c51bd-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="c51bd-194">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="c51bd-194">Update</span></span>
<span data-ttu-id="c51bd-195">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c51bd-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="c51bd-196">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="c51bd-196">In this module administrators can:</span></span>
- <span data-ttu-id="c51bd-197">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="c51bd-197">List and install available updates</span></span>
- <span data-ttu-id="c51bd-198">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="c51bd-198">Resume interrupted updates</span></span>
- <span data-ttu-id="c51bd-199">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="c51bd-199">View installed updates</span></span>
