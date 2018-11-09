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
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274334"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="bc9bd-103">Moduł usługi Azure Stack w wersji 1.3.0</span><span class="sxs-lookup"><span data-stu-id="bc9bd-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9bd-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-104">Requirements:</span></span>
<span data-ttu-id="bc9bd-105">Minimalna obsługiwana wersja usługi Azure Stack to 1804.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="bc9bd-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="bc9bd-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="bc9bd-107">Znane problemy:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-107">Known issues:</span></span>

- <span data-ttu-id="bc9bd-108">Alert dotyczący zamknięcia wymaga usługi Azure Stack w wersji 1803.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="bc9bd-109">Niektóre polecenia cmdlet modułu Storage wymagają usługi Azure Stack w wersji 1804.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="bc9bd-110">Polecenie New-AzsOffer nie pozwala na utworzenie oferty ze stanem publicznym.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="bc9bd-111">Po jego wykonaniu należy wywołać polecenie cmdlet Set-AzsOffer, aby zmienić stan.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="bc9bd-112">Nie można usunąć puli adresów IP bez ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="bc9bd-113">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="bc9bd-113">Breaking Changes</span></span>
<span data-ttu-id="bc9bd-114">Wszystkie zmiany powodujące niezgodność spowodowane migracją z wersji 1.2.11 są udokumentowane tutaj: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="bc9bd-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="bc9bd-115">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="bc9bd-115">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="bc9bd-116">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="bc9bd-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="bc9bd-117">Azure Bridge</span></span>
<span data-ttu-id="bc9bd-118">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="bc9bd-119">Backup</span><span class="sxs-lookup"><span data-stu-id="bc9bd-119">Backup</span></span>
<span data-ttu-id="bc9bd-120">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="bc9bd-121">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="bc9bd-121">Configure where backups are stored</span></span>
- <span data-ttu-id="bc9bd-122">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="bc9bd-122">Perform backups</span></span>
- <span data-ttu-id="bc9bd-123">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="bc9bd-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="bc9bd-124">Commerce</span><span class="sxs-lookup"><span data-stu-id="bc9bd-124">Commerce</span></span>
<span data-ttu-id="bc9bd-125">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="bc9bd-126">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="bc9bd-126">Compute</span></span>
<span data-ttu-id="bc9bd-127">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="bc9bd-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="bc9bd-128">Fabric</span></span>
<span data-ttu-id="bc9bd-129">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="bc9bd-130">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="bc9bd-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="bc9bd-131">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="bc9bd-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="bc9bd-132">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="bc9bd-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="bc9bd-133">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="bc9bd-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="bc9bd-134">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="bc9bd-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="bc9bd-135">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="bc9bd-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="bc9bd-136">Galeria</span><span class="sxs-lookup"><span data-stu-id="bc9bd-136">Gallery</span></span>
<span data-ttu-id="bc9bd-137">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="bc9bd-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="bc9bd-138">Infrastructure Insights</span></span>
<span data-ttu-id="bc9bd-139">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="bc9bd-140">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="bc9bd-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="bc9bd-141">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="bc9bd-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="bc9bd-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bc9bd-142">KeyVault</span></span>
<span data-ttu-id="bc9bd-143">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="bc9bd-144">Sieć</span><span class="sxs-lookup"><span data-stu-id="bc9bd-144">Network</span></span>
<span data-ttu-id="bc9bd-145">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="bc9bd-146">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="bc9bd-146">Management of network quotas</span></span>
- <span data-ttu-id="bc9bd-147">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="bc9bd-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="bc9bd-148">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="bc9bd-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="bc9bd-149">Magazyn</span><span class="sxs-lookup"><span data-stu-id="bc9bd-149">Storage</span></span>
<span data-ttu-id="bc9bd-150">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="bc9bd-151">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="bc9bd-152">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="bc9bd-152">Manage storage quotas</span></span>
- <span data-ttu-id="bc9bd-153">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="bc9bd-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="bc9bd-154">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="bc9bd-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="bc9bd-155">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="bc9bd-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="bc9bd-156">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="bc9bd-156">View information about the individual storage components</span></span>
- <span data-ttu-id="bc9bd-157">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="bc9bd-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="bc9bd-158">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="bc9bd-158">Subscription Admin</span></span>
<span data-ttu-id="bc9bd-159">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="bc9bd-160">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="bc9bd-161">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="bc9bd-161">Manage plans and offers</span></span>
- <span data-ttu-id="bc9bd-162">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="bc9bd-162">View usage and performance information</span></span>
- <span data-ttu-id="bc9bd-163">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="bc9bd-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="bc9bd-164">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="bc9bd-164">Subscription</span></span>
<span data-ttu-id="bc9bd-165">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="bc9bd-166">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="bc9bd-167">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bc9bd-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="bc9bd-168">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="bc9bd-168">Update</span></span>
<span data-ttu-id="bc9bd-169">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bc9bd-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="bc9bd-170">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="bc9bd-170">In this module administrators can:</span></span>
- <span data-ttu-id="bc9bd-171">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="bc9bd-171">List and install available updates</span></span>
- <span data-ttu-id="bc9bd-172">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="bc9bd-172">Resume interrupted updates</span></span>
- <span data-ttu-id="bc9bd-173">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="bc9bd-173">View installed updates</span></span>
