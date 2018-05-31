# <a name="azure-stack-module-130"></a><span data-ttu-id="afb16-101">Moduł usługi Azure Stack w wersji 1.3.0</span><span class="sxs-lookup"><span data-stu-id="afb16-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="afb16-102">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="afb16-102">Requirements:</span></span>
<span data-ttu-id="afb16-103">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="afb16-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="afb16-104">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="afb16-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="afb16-105">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="afb16-105">Known issues:</span></span>

- <span data-ttu-id="afb16-106">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="afb16-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="afb16-107">Niektóre polecenia cmdlet modułu Storage wymagają usługi Azure Stack w wersji 1804.</span><span class="sxs-lookup"><span data-stu-id="afb16-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="afb16-108">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="afb16-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="afb16-109">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="afb16-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="afb16-110">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="afb16-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="afb16-111">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="afb16-111">Breaking Changes</span></span>
<span data-ttu-id="afb16-112">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="afb16-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="afb16-113">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="afb16-113">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="afb16-114">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="afb16-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="afb16-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="afb16-115">Azure Bridge</span></span>
<span data-ttu-id="afb16-116">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afb16-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="afb16-117">Backup</span><span class="sxs-lookup"><span data-stu-id="afb16-117">Backup</span></span>
<span data-ttu-id="afb16-118">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="afb16-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="afb16-119">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="afb16-119">Configure where backups are stored</span></span>
- <span data-ttu-id="afb16-120">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="afb16-120">Perform backups</span></span>
- <span data-ttu-id="afb16-121">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="afb16-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="afb16-122">Commerce</span><span class="sxs-lookup"><span data-stu-id="afb16-122">Commerce</span></span>
<span data-ttu-id="afb16-123">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="afb16-124">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="afb16-124">Compute</span></span>
<span data-ttu-id="afb16-125">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="afb16-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="afb16-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="afb16-126">Fabric</span></span>
<span data-ttu-id="afb16-127">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="afb16-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="afb16-128">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="afb16-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="afb16-129">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="afb16-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="afb16-130">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="afb16-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="afb16-131">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="afb16-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="afb16-132">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="afb16-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="afb16-133">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="afb16-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="afb16-134">Galeria</span><span class="sxs-lookup"><span data-stu-id="afb16-134">Gallery</span></span>
<span data-ttu-id="afb16-135">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="afb16-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="afb16-136">Infrastructure Insights</span></span>
<span data-ttu-id="afb16-137">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="afb16-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="afb16-138">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="afb16-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="afb16-139">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="afb16-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="afb16-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="afb16-140">KeyVault</span></span>
<span data-ttu-id="afb16-141">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="afb16-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="afb16-142">Sieć</span><span class="sxs-lookup"><span data-stu-id="afb16-142">Network</span></span>
<span data-ttu-id="afb16-143">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="afb16-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="afb16-144">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="afb16-144">Management of network quotas</span></span>
- <span data-ttu-id="afb16-145">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="afb16-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="afb16-146">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="afb16-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="afb16-147">Magazyn</span><span class="sxs-lookup"><span data-stu-id="afb16-147">Storage</span></span>
<span data-ttu-id="afb16-148">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="afb16-149">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="afb16-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="afb16-150">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="afb16-150">Manage storage quotas</span></span>
- <span data-ttu-id="afb16-151">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="afb16-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="afb16-152">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="afb16-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="afb16-153">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="afb16-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="afb16-154">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="afb16-154">View information about the individual storage components</span></span>
- <span data-ttu-id="afb16-155">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="afb16-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="afb16-156">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="afb16-156">Subscription Admin</span></span>
<span data-ttu-id="afb16-157">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="afb16-158">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="afb16-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="afb16-159">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="afb16-159">Manage plans and offers</span></span>
- <span data-ttu-id="afb16-160">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="afb16-160">View usage and performance information</span></span>
- <span data-ttu-id="afb16-161">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="afb16-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="afb16-162">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="afb16-162">Subscription</span></span>
<span data-ttu-id="afb16-163">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="afb16-164">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="afb16-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="afb16-165">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="afb16-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="afb16-166">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="afb16-166">Update</span></span>
<span data-ttu-id="afb16-167">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="afb16-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="afb16-168">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="afb16-168">In this module administrators can:</span></span>
- <span data-ttu-id="afb16-169">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="afb16-169">List and install available updates</span></span>
- <span data-ttu-id="afb16-170">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="afb16-170">Resume interrupted updates</span></span>
- <span data-ttu-id="afb16-171">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="afb16-171">View installed updates</span></span>
