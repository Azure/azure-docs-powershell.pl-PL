---
title: Omówienie programu Azure Stack PowerShell | Microsoft Docs
description: Omówienie programu Azure Stack PowerShell z instrukcjami dotyczącymi instalacji i konfiguracji.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50026860"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="9df26-103">Moduł AzureRM 2.3.0</span><span class="sxs-lookup"><span data-stu-id="9df26-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="9df26-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="9df26-104">Requirements:</span></span>
<span data-ttu-id="9df26-105">Minimalna obsługiwana wersja usługi Azure Stack to 1808.</span><span class="sxs-lookup"><span data-stu-id="9df26-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="9df26-106">Uwaga: jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="9df26-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="9df26-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="9df26-107">Install</span></span>
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a><span data-ttu-id="9df26-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="9df26-108">Release Notes</span></span>
* <span data-ttu-id="9df26-109">Wersja 2.3.0 zawiera listę zmian powodujących niezgodność.</span><span class="sxs-lookup"><span data-stu-id="9df26-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="9df26-110">Aby uaktualnić z wersji 1.2.11, skorzystaj z przygotowanego przez nas przewodnika po migracji dostępnego pod adresem https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="9df26-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="9df26-111">Ta wersja odpowiada specyficznemu dla usługi Azure Stack profilowi interfejsu API o nazwie 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="9df26-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="9df26-112">Wszystkie moduły mają taką samą lub większą zależność od modułu AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="9df26-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="9df26-113">Wersje interfejsu API obsługiwane przez poszczególne moduły zostały zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="9df26-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="9df26-114">Obliczenia — 30.03.2017</span><span class="sxs-lookup"><span data-stu-id="9df26-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="9df26-115">Sieć — 01.10.2017</span><span class="sxs-lookup"><span data-stu-id="9df26-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="9df26-116">Magazyn — 01.01.2016</span><span class="sxs-lookup"><span data-stu-id="9df26-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="9df26-117">Zasoby — 01.02.2018</span><span class="sxs-lookup"><span data-stu-id="9df26-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="9df26-118">Magazyn kluczy — 01.10.2016</span><span class="sxs-lookup"><span data-stu-id="9df26-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="9df26-119">DNS — 01.04.2016</span><span class="sxs-lookup"><span data-stu-id="9df26-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="9df26-120">Pełną mapę wersji interfejsu API dla poszczególnych typów zasobów można znaleźć pod adresem https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="9df26-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="9df26-121">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="9df26-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="9df26-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="9df26-122">Azure Bridge</span></span>
<span data-ttu-id="9df26-123">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9df26-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="9df26-124">Backup</span><span class="sxs-lookup"><span data-stu-id="9df26-124">Backup</span></span>
<span data-ttu-id="9df26-125">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="9df26-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="9df26-126">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="9df26-126">Configure where backups are stored</span></span>
- <span data-ttu-id="9df26-127">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="9df26-127">Perform backups</span></span>
- <span data-ttu-id="9df26-128">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="9df26-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="9df26-129">Commerce</span><span class="sxs-lookup"><span data-stu-id="9df26-129">Commerce</span></span>
<span data-ttu-id="9df26-130">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="9df26-131">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="9df26-131">Compute</span></span>
<span data-ttu-id="9df26-132">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy, dyskami zarządzanymi oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="9df26-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="9df26-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="9df26-133">Fabric</span></span>
<span data-ttu-id="9df26-134">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="9df26-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="9df26-135">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="9df26-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="9df26-136">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="9df26-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="9df26-137">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="9df26-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="9df26-138">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="9df26-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="9df26-139">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="9df26-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="9df26-140">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="9df26-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="9df26-141">Galeria</span><span class="sxs-lookup"><span data-stu-id="9df26-141">Gallery</span></span>
<span data-ttu-id="9df26-142">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="9df26-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="9df26-143">Infrastructure Insights</span></span>
<span data-ttu-id="9df26-144">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="9df26-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="9df26-145">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="9df26-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="9df26-146">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="9df26-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="9df26-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9df26-147">KeyVault</span></span>
<span data-ttu-id="9df26-148">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9df26-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="9df26-149">Sieć</span><span class="sxs-lookup"><span data-stu-id="9df26-149">Network</span></span>
<span data-ttu-id="9df26-150">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="9df26-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="9df26-151">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="9df26-151">Management of network quotas</span></span>
- <span data-ttu-id="9df26-152">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9df26-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="9df26-153">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="9df26-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="9df26-154">Magazyn</span><span class="sxs-lookup"><span data-stu-id="9df26-154">Storage</span></span>
<span data-ttu-id="9df26-155">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="9df26-156">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="9df26-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="9df26-157">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="9df26-157">Manage storage quotas</span></span>
- <span data-ttu-id="9df26-158">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="9df26-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="9df26-159">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="9df26-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="9df26-160">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="9df26-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="9df26-161">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="9df26-161">View information about the individual storage components</span></span>
- <span data-ttu-id="9df26-162">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="9df26-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="9df26-163">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="9df26-163">Subscription Admin</span></span>
<span data-ttu-id="9df26-164">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="9df26-165">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="9df26-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="9df26-166">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="9df26-166">Manage plans and offers</span></span>
- <span data-ttu-id="9df26-167">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="9df26-167">View usage and performance information</span></span>
- <span data-ttu-id="9df26-168">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="9df26-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="9df26-169">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="9df26-169">Subscription</span></span>
<span data-ttu-id="9df26-170">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="9df26-171">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="9df26-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="9df26-172">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9df26-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="9df26-173">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="9df26-173">Update</span></span>
<span data-ttu-id="9df26-174">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="9df26-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="9df26-175">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="9df26-175">In this module administrators can:</span></span>
- <span data-ttu-id="9df26-176">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="9df26-176">List and install available updates</span></span>
- <span data-ttu-id="9df26-177">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="9df26-177">Resume interrupted updates</span></span>
- <span data-ttu-id="9df26-178">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="9df26-178">View installed updates</span></span>
