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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038197"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="3d51e-103">Moduł AzureRM 2.5.0</span><span class="sxs-lookup"><span data-stu-id="3d51e-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="3d51e-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="3d51e-104">Requirements:</span></span>
<span data-ttu-id="3d51e-105">Minimalna obsługiwana wersja usługi Azure Stack to 1904.</span><span class="sxs-lookup"><span data-stu-id="3d51e-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="3d51e-106">Uwaga: Jeśli używasz starszej wersji, zainstaluj wersję 1.2.11</span><span class="sxs-lookup"><span data-stu-id="3d51e-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="3d51e-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="3d51e-107">Install</span></span>
```powershell-interactive
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

## <a name="release-notes"></a><span data-ttu-id="3d51e-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="3d51e-108">Release Notes</span></span>
* <span data-ttu-id="3d51e-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="3d51e-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="3d51e-110">Nowy moduł zasobów obsługujący wersję interfejsu API 2018-05-01 z profilem 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="3d51e-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="3d51e-111">Operacje PolicyDefinition(2016-12-01) i PolicyAssisgment(2017-06-01-preview) są nadal wykonywane przy użyciu starych wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="3d51e-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="3d51e-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="3d51e-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="3d51e-113">Nowy moduł obliczeniowy obsługujący wersję interfejsu API 2017-12-01.</span><span class="sxs-lookup"><span data-stu-id="3d51e-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="3d51e-114">Ta wersja odpowiada specyficznemu dla usługi Azure Stack profilowi interfejsu API o nazwie 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="3d51e-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="3d51e-115">Wszystkie moduły mają taką samą lub większą zależność od modułu AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="3d51e-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="3d51e-116">Wersje interfejsu API obsługiwane przez poszczególne moduły zostały zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="3d51e-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="3d51e-117">Obliczenia — 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="3d51e-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="3d51e-118">Sieć — 01.10.2017</span><span class="sxs-lookup"><span data-stu-id="3d51e-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="3d51e-119">Magazyn — 01.01.2016</span><span class="sxs-lookup"><span data-stu-id="3d51e-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="3d51e-120">Zasoby — 01.02.2018</span><span class="sxs-lookup"><span data-stu-id="3d51e-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="3d51e-121">Magazyn kluczy — 01.10.2016</span><span class="sxs-lookup"><span data-stu-id="3d51e-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="3d51e-122">DNS — 01.04.2016</span><span class="sxs-lookup"><span data-stu-id="3d51e-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="3d51e-123">Pełną mapę wersji interfejsu API dla poszczególnych typów zasobów można znaleźć pod adresem https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="3d51e-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="3d51e-124">Zawartość:</span><span class="sxs-lookup"><span data-stu-id="3d51e-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="3d51e-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="3d51e-125">Azure Bridge</span></span>
<span data-ttu-id="3d51e-126">Wersja zapoznawcza modułu administratora Azure Bridge usługi Azure Stack, dzięki któremu można przeprowadzać syndykację obrazów z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d51e-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="3d51e-127">Backup</span><span class="sxs-lookup"><span data-stu-id="3d51e-127">Backup</span></span>
<span data-ttu-id="3d51e-128">Wersja zapoznawcza modułu administratora Backup, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="3d51e-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="3d51e-129">Konfigurowanie miejsca przechowywania kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="3d51e-129">Configure where backups are stored</span></span>
- <span data-ttu-id="3d51e-130">Wykonywanie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="3d51e-130">Perform backups</span></span>
- <span data-ttu-id="3d51e-131">Wyświetlanie listy ukończonych kopii zapasowych i przywracanie ich</span><span class="sxs-lookup"><span data-stu-id="3d51e-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="3d51e-132">Commerce</span><span class="sxs-lookup"><span data-stu-id="3d51e-132">Commerce</span></span>
<span data-ttu-id="3d51e-133">Wersja zapoznawcza modułu administratora Commerce usługi Azure Stack, który umożliwia wyświetlanie zagregowanego użycia danych w całym systemie usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="3d51e-134">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="3d51e-134">Compute</span></span>
<span data-ttu-id="3d51e-135">Wersja zapoznawcza modułu administratora Compute usługi Azure Stack, który udostępnia funkcje zarządzania limitami przydziału zasobów obliczeniowych, obrazami platformy, dyskami zarządzanymi oraz rozszerzeniami maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3d51e-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="3d51e-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="3d51e-136">Fabric</span></span>
<span data-ttu-id="3d51e-137">Wersja zapoznawcza modułu administratora Fabric usługi Azure Stack, który pozwala administratorom na wyświetlanie składników infrastruktury i zarządzanie nimi:</span><span class="sxs-lookup"><span data-stu-id="3d51e-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="3d51e-138">Zatrzymywanie, uruchamianie i zamykanie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="3d51e-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="3d51e-139">Opróżnianie i wznawianie węzłów jednostki skalowania na potrzeby działań związanych z jednostką wymienną</span><span class="sxs-lookup"><span data-stu-id="3d51e-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="3d51e-140">Naprawianie węzłów jednostki skalowania</span><span class="sxs-lookup"><span data-stu-id="3d51e-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="3d51e-141">Ponowne uruchamianie roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="3d51e-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="3d51e-142">Zatrzymywanie, uruchamianie i zamykanie wystąpień roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="3d51e-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="3d51e-143">Tworzenie nowych pul adresów IP</span><span class="sxs-lookup"><span data-stu-id="3d51e-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="3d51e-144">Galeria</span><span class="sxs-lookup"><span data-stu-id="3d51e-144">Gallery</span></span>
<span data-ttu-id="3d51e-145">Wersja zapoznawcza modułu administratora Gallery usługi Azure Stack, który udostępnia funkcje zarządzania elementami galerii na platformie handlowej usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="3d51e-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="3d51e-146">Infrastructure Insights</span></span>
<span data-ttu-id="3d51e-147">Wersja zapoznawcza modułu administratora Infrastructure Insights, który pozwala administratorom na:</span><span class="sxs-lookup"><span data-stu-id="3d51e-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="3d51e-148">Wyświetlanie informacji o kondycji zasobów sprzętowych usługi Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3d51e-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="3d51e-149">Wyświetlanie alertów i zarządzanie nimi</span><span class="sxs-lookup"><span data-stu-id="3d51e-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="3d51e-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d51e-150">KeyVault</span></span>
<span data-ttu-id="3d51e-151">Wersja zapoznawcza modułu administratora KeyVault usługi Azure Stack, który pozwala administratorowi na wyświetlanie limitów przydziału magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3d51e-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="3d51e-152">Sieć</span><span class="sxs-lookup"><span data-stu-id="3d51e-152">Network</span></span>
<span data-ttu-id="3d51e-153">Wersja zapoznawcza modułu administratora Network, który pozwala na:</span><span class="sxs-lookup"><span data-stu-id="3d51e-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="3d51e-154">Zarządzanie limitami przydziału sieci</span><span class="sxs-lookup"><span data-stu-id="3d51e-154">Management of network quotas</span></span>
- <span data-ttu-id="3d51e-155">Wyświetlanie przydzielonych zasobów sieciowych, takich jak publiczne adresy IP, sieci wirtualne oraz moduły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3d51e-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="3d51e-156">Korzystanie z polecenia cmdlet, które wyświetla przegląd administratora</span><span class="sxs-lookup"><span data-stu-id="3d51e-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="3d51e-157">Magazyn</span><span class="sxs-lookup"><span data-stu-id="3d51e-157">Storage</span></span>
<span data-ttu-id="3d51e-158">Wersja zapoznawcza modułu administratora Storage usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="3d51e-159">W tej wersji udostępniamy następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="3d51e-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="3d51e-160">Zarządzanie limitami przydziału magazynu</span><span class="sxs-lookup"><span data-stu-id="3d51e-160">Manage storage quotas</span></span>
- <span data-ttu-id="3d51e-161">Odzyskiwanie pamięci w przypadku usuniętych zasobów magazynu</span><span class="sxs-lookup"><span data-stu-id="3d51e-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="3d51e-162">Przywracanie usuniętych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="3d51e-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="3d51e-163">Migrowanie kontenerów między udziałami</span><span class="sxs-lookup"><span data-stu-id="3d51e-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="3d51e-164">Wyświetlanie informacji o pojedynczych składnikach magazynu</span><span class="sxs-lookup"><span data-stu-id="3d51e-164">View information about the individual storage components</span></span>
- <span data-ttu-id="3d51e-165">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="3d51e-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="3d51e-166">Subscription (administrator)</span><span class="sxs-lookup"><span data-stu-id="3d51e-166">Subscription Admin</span></span>
<span data-ttu-id="3d51e-167">Wersja zapoznawcza modułu administratora Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="3d51e-168">Ten moduł udostępnia administratorom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="3d51e-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="3d51e-169">Zarządzanie planami i ofertami</span><span class="sxs-lookup"><span data-stu-id="3d51e-169">Manage plans and offers</span></span>
- <span data-ttu-id="3d51e-170">Wyświetlanie informacji dotyczących użycia i wydajności</span><span class="sxs-lookup"><span data-stu-id="3d51e-170">View usage and performance information</span></span>
- <span data-ttu-id="3d51e-171">Zarządzanie kontrolą dostępu opartą na rolach</span><span class="sxs-lookup"><span data-stu-id="3d51e-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="3d51e-172">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="3d51e-172">Subscription</span></span>
<span data-ttu-id="3d51e-173">Wersja zapoznawcza modułu Subscription usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="3d51e-174">Ten moduł udostępnia użytkownikom następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="3d51e-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="3d51e-175">Tworzenie, usuwanie i aktualizowanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3d51e-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="3d51e-176">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="3d51e-176">Update</span></span>
<span data-ttu-id="3d51e-177">Wersja zapoznawcza modułu administratora Update usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3d51e-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="3d51e-178">W tym module administratorzy mogą wykonywać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="3d51e-178">In this module administrators can:</span></span>
- <span data-ttu-id="3d51e-179">Wyświetlanie listy dostępnych aktualizacji oraz instalowanie ich</span><span class="sxs-lookup"><span data-stu-id="3d51e-179">List and install available updates</span></span>
- <span data-ttu-id="3d51e-180">Wznawianie przerwanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="3d51e-180">Resume interrupted updates</span></span>
- <span data-ttu-id="3d51e-181">Wyświetlanie zainstalowanych aktualizacji</span><span class="sxs-lookup"><span data-stu-id="3d51e-181">View installed updates</span></span>
