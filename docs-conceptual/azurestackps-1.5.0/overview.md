---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053362"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="ad377-103">Moduł usługi Azure Stack w wersji 1.5.0</span><span class="sxs-lookup"><span data-stu-id="ad377-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ad377-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="ad377-104">Requirements:</span></span>
<span data-ttu-id="ad377-105">Minimalna obsługiwana wersja usługi Azure Stack to 1808.</span><span class="sxs-lookup"><span data-stu-id="ad377-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="ad377-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.4.0</span><span class="sxs-lookup"><span data-stu-id="ad377-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="ad377-107">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="ad377-107">Known issues:</span></span>

- <span data-ttu-id="ad377-108">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="ad377-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ad377-109">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="ad377-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ad377-110">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ad377-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="ad377-111">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="ad377-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="ad377-112">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="ad377-112">Release Notes</span></span>
* <span data-ttu-id="ad377-113">Wszystkie moduły administratora usługi Azure Stack zostały zaktualizowane pod kątem uzyskania takiej samej lub większej zależności od modułu AzureRm.Profile</span><span class="sxs-lookup"><span data-stu-id="ad377-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="ad377-114">Obsługa zarządzania nazwami zasobów zagnieżdżonych we wszystkich modułach</span><span class="sxs-lookup"><span data-stu-id="ad377-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="ad377-115">We wszystkich modułach naprawiono usterkę polegającą na tym, że element ErrorActionPreference jest zastępowany w celu zatrzymania</span><span class="sxs-lookup"><span data-stu-id="ad377-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="ad377-116">Moduł Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="ad377-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="ad377-117">Dodano nowe właściwości limitu przydziału na potrzeby obsługi dysku zarządzanego</span><span class="sxs-lookup"><span data-stu-id="ad377-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="ad377-118">Dodano polecenia cmdlet powiązane z migracją dysku</span><span class="sxs-lookup"><span data-stu-id="ad377-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="ad377-119">Dodatkowe właściwości w obiektach rozszerzeń maszyny wirtualnej i obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="ad377-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="ad377-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="ad377-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="ad377-121">Nowe polecenie cmdlet umożliwiające dodawanie węzła jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="ad377-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="ad377-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="ad377-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="ad377-123">Polecenie Set-AzsBackupShare jest teraz aliasem polecenia cmdlet Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad377-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ad377-124">Polecenie Get-AzsBackupLocation jest teraz aliasem polecenia cmdlet Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad377-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ad377-125">Set-AzsBackupConfiguration, parametr BackupShare jest teraz aliasem ścieżki parametru</span><span class="sxs-lookup"><span data-stu-id="ad377-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="ad377-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="ad377-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="ad377-127">Get-AzsDelegatedProviderOffer, parametr OfferName jest teraz aliasem parametru Offer</span><span class="sxs-lookup"><span data-stu-id="ad377-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="ad377-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="ad377-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="ad377-129">Get-AzsDelegatedProviderOffer, parametr OfferName jest teraz aliasem parametru Offer</span><span class="sxs-lookup"><span data-stu-id="ad377-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="ad377-130">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="ad377-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ad377-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ad377-131">Azure Bridge</span></span>
<span data-ttu-id="ad377-132">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad377-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ad377-133">Backup</span><span class="sxs-lookup"><span data-stu-id="ad377-133">Backup</span></span>
<span data-ttu-id="ad377-134">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="ad377-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ad377-135">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="ad377-135">Configure where backups are stored</span></span>
- <span data-ttu-id="ad377-136">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="ad377-136">Perform backups</span></span>
- <span data-ttu-id="ad377-137">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="ad377-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ad377-138">Commerce</span><span class="sxs-lookup"><span data-stu-id="ad377-138">Commerce</span></span>
<span data-ttu-id="ad377-139">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ad377-140">Compute</span><span class="sxs-lookup"><span data-stu-id="ad377-140">Compute</span></span>
<span data-ttu-id="ad377-141">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy, dyskami zarządzanymi oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="ad377-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ad377-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="ad377-142">Fabric</span></span>
<span data-ttu-id="ad377-143">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="ad377-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ad377-144">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="ad377-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ad377-145">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="ad377-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ad377-146">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="ad377-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ad377-147">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="ad377-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ad377-148">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="ad377-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ad377-149">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="ad377-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ad377-150">Galeria</span><span class="sxs-lookup"><span data-stu-id="ad377-150">Gallery</span></span>
<span data-ttu-id="ad377-151">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ad377-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="ad377-152">Infrastructure Insights</span></span>
<span data-ttu-id="ad377-153">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="ad377-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ad377-154">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="ad377-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ad377-155">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="ad377-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ad377-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad377-156">KeyVault</span></span>
<span data-ttu-id="ad377-157">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="ad377-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ad377-158">Network</span><span class="sxs-lookup"><span data-stu-id="ad377-158">Network</span></span>
<span data-ttu-id="ad377-159">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="ad377-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ad377-160">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="ad377-160">Management of network quotas</span></span>
- <span data-ttu-id="ad377-161">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ad377-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ad377-162">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="ad377-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ad377-163">Storage</span><span class="sxs-lookup"><span data-stu-id="ad377-163">Storage</span></span>
<span data-ttu-id="ad377-164">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ad377-165">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="ad377-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ad377-166">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="ad377-166">Manage storage quotas</span></span>
- <span data-ttu-id="ad377-167">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="ad377-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ad377-168">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="ad377-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ad377-169">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="ad377-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ad377-170">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="ad377-170">View information about the individual storage components</span></span>
- <span data-ttu-id="ad377-171">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="ad377-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ad377-172">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="ad377-172">Subscription Admin</span></span>
<span data-ttu-id="ad377-173">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ad377-174">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="ad377-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ad377-175">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="ad377-175">Manage plans and offers</span></span>
- <span data-ttu-id="ad377-176">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="ad377-176">View usage and performance information</span></span>
- <span data-ttu-id="ad377-177">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="ad377-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ad377-178">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="ad377-178">Subscription</span></span>
<span data-ttu-id="ad377-179">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ad377-180">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="ad377-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ad377-181">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ad377-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ad377-182">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="ad377-182">Update</span></span>
<span data-ttu-id="ad377-183">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ad377-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ad377-184">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="ad377-184">In this module administrators can:</span></span>
- <span data-ttu-id="ad377-185">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="ad377-185">List and install available updates</span></span>
- <span data-ttu-id="ad377-186">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="ad377-186">Resume interrupted updates</span></span>
- <span data-ttu-id="ad377-187">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="ad377-187">View installed updates</span></span>
