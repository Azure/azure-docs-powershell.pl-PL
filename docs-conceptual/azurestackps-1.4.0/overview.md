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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424857"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="66ce6-103">Moduł usługi Azure Stack w wersji 1.4.0</span><span class="sxs-lookup"><span data-stu-id="66ce6-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="66ce6-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="66ce6-104">Requirements:</span></span>
<span data-ttu-id="66ce6-105">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="66ce6-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="66ce6-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="66ce6-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="66ce6-107">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="66ce6-107">Known issues:</span></span>

- <span data-ttu-id="66ce6-108">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="66ce6-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="66ce6-109">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="66ce6-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="66ce6-110">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="66ce6-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="66ce6-111">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="66ce6-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="66ce6-112">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="66ce6-112">Breaking Changes</span></span>
<span data-ttu-id="66ce6-113">Nie ma zmian powodujących niezgodność względem wersji 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="66ce6-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="66ce6-114">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="66ce6-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="66ce6-115">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="66ce6-115">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="66ce6-116">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="66ce6-116">Release Notes</span></span>
    * <span data-ttu-id="66ce6-117">W wersji 1.4.0 usługi Azure Stack nie wprowadzono żadnych zmian powodujących niezgodność z poprzednią wersją, 1.3.0</span><span class="sxs-lookup"><span data-stu-id="66ce6-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="66ce6-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="66ce6-119">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="66ce6-121">Dodano nowe parametry (BackupFrequencyInHours, IsBackupSchedulerEnabled i BackupRetentionPeriodInDays) do polecenia cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="66ce6-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="66ce6-122">Dodano polecenie cmdlet New-EncyptionKeyBase64 ułatwiające tworzenie klucza szyfrowania</span><span class="sxs-lookup"><span data-stu-id="66ce6-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="66ce6-123">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="66ce6-125">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="66ce6-127">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="66ce6-128">Dodano polecenie cmdlet Add-AzsScaleUnitNode, aby umożliwić administratorowi dodawanie nowych węzłów jednostki skalowania do zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="66ce6-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="66ce6-129">Dodano polecenie cmdlet New-AzsScaleUnitNodeObject ułatwiające tworzenie obiektów parametrów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="66ce6-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="66ce6-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="66ce6-131">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="66ce6-133">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="66ce6-135">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="66ce6-137">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="66ce6-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="66ce6-139">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="66ce6-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="66ce6-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="66ce6-141">Dodano polecenie cmdlet Move-AzsSubscription umożliwiające przenoszenie subskrypcji między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="66ce6-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="66ce6-142">Dodano polecenie cmdlet Test-AzsMoveSubscription służące do weryfikowania, czy subskrypcje użytkownika można przenosić między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="66ce6-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="66ce6-143">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="66ce6-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="66ce6-144">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="66ce6-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="66ce6-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="66ce6-145">Azure Bridge</span></span>
<span data-ttu-id="66ce6-146">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="66ce6-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="66ce6-147">Backup</span><span class="sxs-lookup"><span data-stu-id="66ce6-147">Backup</span></span>
<span data-ttu-id="66ce6-148">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="66ce6-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="66ce6-149">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="66ce6-149">Configure where backups are stored</span></span>
- <span data-ttu-id="66ce6-150">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="66ce6-150">Perform backups</span></span>
- <span data-ttu-id="66ce6-151">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="66ce6-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="66ce6-152">Commerce</span><span class="sxs-lookup"><span data-stu-id="66ce6-152">Commerce</span></span>
<span data-ttu-id="66ce6-153">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="66ce6-154">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="66ce6-154">Compute</span></span>
<span data-ttu-id="66ce6-155">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="66ce6-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="66ce6-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="66ce6-156">Fabric</span></span>
<span data-ttu-id="66ce6-157">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="66ce6-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="66ce6-158">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="66ce6-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="66ce6-159">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="66ce6-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="66ce6-160">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="66ce6-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="66ce6-161">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="66ce6-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="66ce6-162">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="66ce6-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="66ce6-163">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="66ce6-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="66ce6-164">Galeria</span><span class="sxs-lookup"><span data-stu-id="66ce6-164">Gallery</span></span>
<span data-ttu-id="66ce6-165">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="66ce6-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="66ce6-166">Infrastructure Insights</span></span>
<span data-ttu-id="66ce6-167">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="66ce6-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="66ce6-168">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="66ce6-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="66ce6-169">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="66ce6-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="66ce6-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="66ce6-170">KeyVault</span></span>
<span data-ttu-id="66ce6-171">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="66ce6-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="66ce6-172">Sieć</span><span class="sxs-lookup"><span data-stu-id="66ce6-172">Network</span></span>
<span data-ttu-id="66ce6-173">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="66ce6-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="66ce6-174">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="66ce6-174">Management of network quotas</span></span>
- <span data-ttu-id="66ce6-175">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="66ce6-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="66ce6-176">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="66ce6-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="66ce6-177">Magazyn</span><span class="sxs-lookup"><span data-stu-id="66ce6-177">Storage</span></span>
<span data-ttu-id="66ce6-178">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="66ce6-179">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="66ce6-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="66ce6-180">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="66ce6-180">Manage storage quotas</span></span>
- <span data-ttu-id="66ce6-181">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="66ce6-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="66ce6-182">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="66ce6-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="66ce6-183">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="66ce6-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="66ce6-184">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="66ce6-184">View information about the individual storage components</span></span>
- <span data-ttu-id="66ce6-185">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="66ce6-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="66ce6-186">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="66ce6-186">Subscription Admin</span></span>
<span data-ttu-id="66ce6-187">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="66ce6-188">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="66ce6-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="66ce6-189">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="66ce6-189">Manage plans and offers</span></span>
- <span data-ttu-id="66ce6-190">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="66ce6-190">View usage and performance information</span></span>
- <span data-ttu-id="66ce6-191">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="66ce6-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="66ce6-192">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="66ce6-192">Subscription</span></span>
<span data-ttu-id="66ce6-193">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="66ce6-194">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="66ce6-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="66ce6-195">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="66ce6-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="66ce6-196">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="66ce6-196">Update</span></span>
<span data-ttu-id="66ce6-197">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="66ce6-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="66ce6-198">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="66ce6-198">In this module administrators can:</span></span>
- <span data-ttu-id="66ce6-199">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="66ce6-199">List and install available updates</span></span>
- <span data-ttu-id="66ce6-200">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="66ce6-200">Resume interrupted updates</span></span>
- <span data-ttu-id="66ce6-201">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="66ce6-201">View installed updates</span></span>
