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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211982"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="e7e2d-103">Moduł usługi Azure Stack w wersji 1.3.0</span><span class="sxs-lookup"><span data-stu-id="e7e2d-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e2d-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-104">Requirements:</span></span>
<span data-ttu-id="e7e2d-105">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="e7e2d-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="e7e2d-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="e7e2d-107">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-107">Known issues:</span></span>

- <span data-ttu-id="e7e2d-108">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="e7e2d-109">Niektóre polecenia cmdlet modułu Storage wymagają usługi Azure Stack w wersji 1804.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="e7e2d-110">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="e7e2d-111">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="e7e2d-112">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="e7e2d-113">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="e7e2d-113">Breaking Changes</span></span>
<span data-ttu-id="e7e2d-114">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="e7e2d-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="e7e2d-115">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="e7e2d-115">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="e7e2d-116">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="e7e2d-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="e7e2d-117">Azure Bridge</span></span>
<span data-ttu-id="e7e2d-118">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="e7e2d-119">Backup</span><span class="sxs-lookup"><span data-stu-id="e7e2d-119">Backup</span></span>
<span data-ttu-id="e7e2d-120">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="e7e2d-121">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="e7e2d-121">Configure where backups are stored</span></span>
- <span data-ttu-id="e7e2d-122">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="e7e2d-122">Perform backups</span></span>
- <span data-ttu-id="e7e2d-123">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="e7e2d-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="e7e2d-124">Commerce</span><span class="sxs-lookup"><span data-stu-id="e7e2d-124">Commerce</span></span>
<span data-ttu-id="e7e2d-125">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="e7e2d-126">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="e7e2d-126">Compute</span></span>
<span data-ttu-id="e7e2d-127">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="e7e2d-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="e7e2d-128">Fabric</span></span>
<span data-ttu-id="e7e2d-129">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="e7e2d-130">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="e7e2d-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="e7e2d-131">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="e7e2d-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="e7e2d-132">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="e7e2d-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="e7e2d-133">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="e7e2d-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="e7e2d-134">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="e7e2d-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="e7e2d-135">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="e7e2d-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="e7e2d-136">Galeria</span><span class="sxs-lookup"><span data-stu-id="e7e2d-136">Gallery</span></span>
<span data-ttu-id="e7e2d-137">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="e7e2d-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="e7e2d-138">Infrastructure Insights</span></span>
<span data-ttu-id="e7e2d-139">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="e7e2d-140">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="e7e2d-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="e7e2d-141">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="e7e2d-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="e7e2d-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e7e2d-142">KeyVault</span></span>
<span data-ttu-id="e7e2d-143">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="e7e2d-144">Sieć</span><span class="sxs-lookup"><span data-stu-id="e7e2d-144">Network</span></span>
<span data-ttu-id="e7e2d-145">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="e7e2d-146">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="e7e2d-146">Management of network quotas</span></span>
- <span data-ttu-id="e7e2d-147">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e7e2d-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="e7e2d-148">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="e7e2d-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="e7e2d-149">Magazyn</span><span class="sxs-lookup"><span data-stu-id="e7e2d-149">Storage</span></span>
<span data-ttu-id="e7e2d-150">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="e7e2d-151">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="e7e2d-152">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="e7e2d-152">Manage storage quotas</span></span>
- <span data-ttu-id="e7e2d-153">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="e7e2d-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="e7e2d-154">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="e7e2d-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="e7e2d-155">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="e7e2d-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="e7e2d-156">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="e7e2d-156">View information about the individual storage components</span></span>
- <span data-ttu-id="e7e2d-157">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="e7e2d-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="e7e2d-158">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="e7e2d-158">Subscription Admin</span></span>
<span data-ttu-id="e7e2d-159">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="e7e2d-160">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="e7e2d-161">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="e7e2d-161">Manage plans and offers</span></span>
- <span data-ttu-id="e7e2d-162">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="e7e2d-162">View usage and performance information</span></span>
- <span data-ttu-id="e7e2d-163">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="e7e2d-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="e7e2d-164">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="e7e2d-164">Subscription</span></span>
<span data-ttu-id="e7e2d-165">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="e7e2d-166">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="e7e2d-167">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e7e2d-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="e7e2d-168">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="e7e2d-168">Update</span></span>
<span data-ttu-id="e7e2d-169">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e7e2d-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="e7e2d-170">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="e7e2d-170">In this module administrators can:</span></span>
- <span data-ttu-id="e7e2d-171">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="e7e2d-171">List and install available updates</span></span>
- <span data-ttu-id="e7e2d-172">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="e7e2d-172">Resume interrupted updates</span></span>
- <span data-ttu-id="e7e2d-173">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="e7e2d-173">View installed updates</span></span>
