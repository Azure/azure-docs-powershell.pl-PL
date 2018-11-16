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
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574672"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="306e0-103">Moduł usługi Azure Stack w wersji 1.4.0</span><span class="sxs-lookup"><span data-stu-id="306e0-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="306e0-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="306e0-104">Requirements:</span></span>
<span data-ttu-id="306e0-105">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="306e0-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="306e0-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="306e0-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="306e0-107">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="306e0-107">Known issues:</span></span>

- <span data-ttu-id="306e0-108">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="306e0-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="306e0-109">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="306e0-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="306e0-110">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="306e0-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="306e0-111">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="306e0-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="306e0-112">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="306e0-112">Breaking Changes</span></span>
<span data-ttu-id="306e0-113">Nie ma zmian powodujących niezgodność względem wersji 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="306e0-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="306e0-114">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="306e0-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="306e0-115">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="306e0-115">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="306e0-116">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="306e0-116">Release Notes</span></span>
    * <span data-ttu-id="306e0-117">W wersji 1.4.0 usługi Azure Stack nie wprowadzono żadnych zmian powodujących niezgodność z poprzednią wersją, 1.3.0</span><span class="sxs-lookup"><span data-stu-id="306e0-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="306e0-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="306e0-119">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="306e0-121">Dodano nowe parametry (BackupFrequencyInHours, IsBackupSchedulerEnabled i BackupRetentionPeriodInDays) do polecenia cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="306e0-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="306e0-122">Dodano polecenie cmdlet New-EncyptionKeyBase64 ułatwiające tworzenie klucza szyfrowania</span><span class="sxs-lookup"><span data-stu-id="306e0-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="306e0-123">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="306e0-125">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="306e0-127">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="306e0-128">Dodano polecenie cmdlet Add-AzsScaleUnitNode, aby umożliwić administratorowi dodawanie nowych węzłów jednostki skalowania do zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="306e0-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="306e0-129">Dodano polecenie cmdlet New-AzsScaleUnitNodeObject ułatwiające tworzenie obiektów parametrów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="306e0-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="306e0-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="306e0-131">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="306e0-133">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="306e0-135">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="306e0-137">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="306e0-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="306e0-139">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="306e0-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="306e0-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="306e0-141">Dodano polecenie cmdlet Move-AzsSubscription umożliwiające przenoszenie subskrypcji między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="306e0-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="306e0-142">Dodano polecenie cmdlet Test-AzsMoveSubscription służące do weryfikowania, czy subskrypcje użytkownika można przenosić między delegowanymi ofertami dostawców</span><span class="sxs-lookup"><span data-stu-id="306e0-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="306e0-143">Naprawienie usterki, która powodowała zwrócenie tylko jednej strony wyników podzielonych na strony</span><span class="sxs-lookup"><span data-stu-id="306e0-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="306e0-144">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="306e0-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="306e0-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="306e0-145">Azure Bridge</span></span>
<span data-ttu-id="306e0-146">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="306e0-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="306e0-147">Backup</span><span class="sxs-lookup"><span data-stu-id="306e0-147">Backup</span></span>
<span data-ttu-id="306e0-148">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="306e0-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="306e0-149">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="306e0-149">Configure where backups are stored</span></span>
- <span data-ttu-id="306e0-150">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="306e0-150">Perform backups</span></span>
- <span data-ttu-id="306e0-151">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="306e0-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="306e0-152">Commerce</span><span class="sxs-lookup"><span data-stu-id="306e0-152">Commerce</span></span>
<span data-ttu-id="306e0-153">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="306e0-154">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="306e0-154">Compute</span></span>
<span data-ttu-id="306e0-155">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="306e0-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="306e0-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="306e0-156">Fabric</span></span>
<span data-ttu-id="306e0-157">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="306e0-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="306e0-158">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="306e0-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="306e0-159">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="306e0-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="306e0-160">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="306e0-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="306e0-161">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="306e0-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="306e0-162">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="306e0-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="306e0-163">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="306e0-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="306e0-164">Galeria</span><span class="sxs-lookup"><span data-stu-id="306e0-164">Gallery</span></span>
<span data-ttu-id="306e0-165">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="306e0-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="306e0-166">Infrastructure Insights</span></span>
<span data-ttu-id="306e0-167">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="306e0-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="306e0-168">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="306e0-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="306e0-169">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="306e0-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="306e0-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="306e0-170">KeyVault</span></span>
<span data-ttu-id="306e0-171">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="306e0-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="306e0-172">Sieć</span><span class="sxs-lookup"><span data-stu-id="306e0-172">Network</span></span>
<span data-ttu-id="306e0-173">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="306e0-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="306e0-174">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="306e0-174">Management of network quotas</span></span>
- <span data-ttu-id="306e0-175">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="306e0-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="306e0-176">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="306e0-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="306e0-177">Magazyn</span><span class="sxs-lookup"><span data-stu-id="306e0-177">Storage</span></span>
<span data-ttu-id="306e0-178">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="306e0-179">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="306e0-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="306e0-180">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="306e0-180">Manage storage quotas</span></span>
- <span data-ttu-id="306e0-181">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="306e0-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="306e0-182">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="306e0-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="306e0-183">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="306e0-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="306e0-184">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="306e0-184">View information about the individual storage components</span></span>
- <span data-ttu-id="306e0-185">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="306e0-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="306e0-186">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="306e0-186">Subscription Admin</span></span>
<span data-ttu-id="306e0-187">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="306e0-188">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="306e0-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="306e0-189">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="306e0-189">Manage plans and offers</span></span>
- <span data-ttu-id="306e0-190">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="306e0-190">View usage and performance information</span></span>
- <span data-ttu-id="306e0-191">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="306e0-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="306e0-192">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="306e0-192">Subscription</span></span>
<span data-ttu-id="306e0-193">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="306e0-194">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="306e0-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="306e0-195">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="306e0-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="306e0-196">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="306e0-196">Update</span></span>
<span data-ttu-id="306e0-197">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="306e0-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="306e0-198">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="306e0-198">In this module administrators can:</span></span>
- <span data-ttu-id="306e0-199">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="306e0-199">List and install available updates</span></span>
- <span data-ttu-id="306e0-200">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="306e0-200">Resume interrupted updates</span></span>
- <span data-ttu-id="306e0-201">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="306e0-201">View installed updates</span></span>
