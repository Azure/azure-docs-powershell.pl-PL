---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117553"
---
# <a name="release-notes"></a><span data-ttu-id="dc5a9-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-103">Release notes</span></span>

<span data-ttu-id="dc5a9-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="dc5a9-105">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dc5a9-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="dc5a9-106">General</span></span>
* <span data-ttu-id="dc5a9-107">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-108">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-109">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="dc5a9-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-110">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-111">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="dc5a9-112">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="dc5a9-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="dc5a9-113">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="dc5a9-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="dc5a9-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="dc5a9-115">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-116">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-117">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="dc5a9-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="dc5a9-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dc5a9-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="dc5a9-119">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="dc5a9-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-120">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-121">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="dc5a9-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc5a9-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="dc5a9-123">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="dc5a9-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dc5a9-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="dc5a9-125">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="dc5a9-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="dc5a9-126">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="dc5a9-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="dc5a9-127">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="dc5a9-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="dc5a9-128">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="dc5a9-129">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="dc5a9-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="dc5a9-130">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="dc5a9-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="dc5a9-131">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="dc5a9-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="dc5a9-132">AzureRM.Websites</span></span>
* <span data-ttu-id="dc5a9-133">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="dc5a9-134">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-135">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-136">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="dc5a9-137">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="dc5a9-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="dc5a9-138">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="dc5a9-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="dc5a9-139">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="dc5a9-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-140">Azure.Storage</span></span>
* <span data-ttu-id="dc5a9-141">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="dc5a9-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="dc5a9-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="dc5a9-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="dc5a9-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="dc5a9-144">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="dc5a9-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="dc5a9-146">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="dc5a9-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc5a9-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="dc5a9-148">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="dc5a9-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="dc5a9-150">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="dc5a9-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="dc5a9-151">AzureRM.Automation</span></span>
* <span data-ttu-id="dc5a9-152">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="dc5a9-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-153">AzureRM.Backup</span></span>
* <span data-ttu-id="dc5a9-154">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="dc5a9-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="dc5a9-155">AzureRM.Batch</span></span>
* <span data-ttu-id="dc5a9-156">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="dc5a9-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="dc5a9-157">AzureRM.Billing</span></span>
* <span data-ttu-id="dc5a9-158">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="dc5a9-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc5a9-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="dc5a9-160">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="dc5a9-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="dc5a9-162">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-163">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-164">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="dc5a9-165">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="dc5a9-166">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="dc5a9-167">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="dc5a9-168">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="dc5a9-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="dc5a9-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="dc5a9-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="dc5a9-170">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="dc5a9-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dc5a9-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="dc5a9-172">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="dc5a9-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="dc5a9-174">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="dc5a9-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="dc5a9-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="dc5a9-176">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="dc5a9-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dc5a9-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="dc5a9-178">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="dc5a9-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dc5a9-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="dc5a9-180">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="dc5a9-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc5a9-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="dc5a9-182">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc5a9-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="dc5a9-183">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="dc5a9-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="dc5a9-184">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="dc5a9-185">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="dc5a9-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="dc5a9-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="dc5a9-187">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="dc5a9-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="dc5a9-188">AzureRM.Dns</span></span>
* <span data-ttu-id="dc5a9-189">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="dc5a9-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc5a9-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="dc5a9-191">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="dc5a9-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="dc5a9-193">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="dc5a9-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc5a9-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="dc5a9-195">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="dc5a9-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-196">AzureRM.Insights</span></span>
* <span data-ttu-id="dc5a9-197">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="dc5a9-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="dc5a9-199">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-201">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="dc5a9-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc5a9-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="dc5a9-203">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="dc5a9-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dc5a9-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="dc5a9-205">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="dc5a9-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="dc5a9-207">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="dc5a9-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dc5a9-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="dc5a9-209">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="dc5a9-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="dc5a9-210">AzureRM.Media</span></span>
* <span data-ttu-id="dc5a9-211">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-212">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-213">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dc5a9-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="dc5a9-214">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dc5a9-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dc5a9-215">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dc5a9-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="dc5a9-216">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="dc5a9-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="dc5a9-217">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="dc5a9-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="dc5a9-218">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dc5a9-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dc5a9-219">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="dc5a9-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="dc5a9-220">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="dc5a9-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="dc5a9-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="dc5a9-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="dc5a9-222">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="dc5a9-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="dc5a9-224">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="dc5a9-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="dc5a9-226">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="dc5a9-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dc5a9-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="dc5a9-228">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="dc5a9-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="dc5a9-230">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="dc5a9-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dc5a9-232">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="dc5a9-233">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="dc5a9-234">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="dc5a9-235">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="dc5a9-236">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="dc5a9-237">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="dc5a9-238">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="dc5a9-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dc5a9-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="dc5a9-240">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="dc5a9-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dc5a9-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="dc5a9-242">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="dc5a9-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="dc5a9-243">AzureRM.Relay</span></span>
* <span data-ttu-id="dc5a9-244">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-245">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-246">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="dc5a9-247">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="dc5a9-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="dc5a9-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="dc5a9-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="dc5a9-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="dc5a9-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="dc5a9-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dc5a9-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="dc5a9-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dc5a9-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="dc5a9-255">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="dc5a9-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="dc5a9-256">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="dc5a9-257">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="dc5a9-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="dc5a9-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="dc5a9-259">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="dc5a9-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc5a9-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="dc5a9-261">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="dc5a9-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc5a9-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="dc5a9-263">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-264">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-265">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="dc5a9-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-266">AzureRM.Storage</span></span>
* <span data-ttu-id="dc5a9-267">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="dc5a9-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="dc5a9-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="dc5a9-269">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="dc5a9-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="dc5a9-270">AzureRM.Tags</span></span>
* <span data-ttu-id="dc5a9-271">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="dc5a9-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dc5a9-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="dc5a9-273">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="dc5a9-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="dc5a9-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="dc5a9-275">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="dc5a9-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="dc5a9-276">AzureRM.Websites</span></span>
* <span data-ttu-id="dc5a9-277">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="dc5a9-278">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dc5a9-279">Ogólne</span><span class="sxs-lookup"><span data-stu-id="dc5a9-279">General</span></span>
* <span data-ttu-id="dc5a9-280">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-281">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-282">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="dc5a9-283">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="dc5a9-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-284">Azure.Storage</span></span>
* <span data-ttu-id="dc5a9-285">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="dc5a9-286">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="dc5a9-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc5a9-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="dc5a9-288">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="dc5a9-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="dc5a9-289">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="dc5a9-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="dc5a9-290">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="dc5a9-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="dc5a9-291">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="dc5a9-292">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="dc5a9-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="dc5a9-293">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="dc5a9-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-294">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-295">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="dc5a9-296">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="dc5a9-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="dc5a9-297">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="dc5a9-298">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="dc5a9-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="dc5a9-299">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="dc5a9-300">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="dc5a9-301">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="dc5a9-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="dc5a9-302">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="dc5a9-303">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="dc5a9-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="dc5a9-304">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="dc5a9-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dc5a9-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="dc5a9-306">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="dc5a9-307">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="dc5a9-308">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="dc5a9-309">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="dc5a9-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc5a9-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="dc5a9-311">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="dc5a9-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="dc5a9-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="dc5a9-313">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="dc5a9-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-314">AzureRM.Insights</span></span>
* <span data-ttu-id="dc5a9-315">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="dc5a9-316">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="dc5a9-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-318">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-319">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-320">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-321">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-322">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="dc5a9-323">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="dc5a9-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc5a9-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="dc5a9-325">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="dc5a9-326">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="dc5a9-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-327">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-328">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="dc5a9-329">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="dc5a9-330">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="dc5a9-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="dc5a9-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="dc5a9-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="dc5a9-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="dc5a9-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="dc5a9-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="dc5a9-334">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc5a9-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="dc5a9-335">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="dc5a9-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="dc5a9-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-336">AzureRM.Storage</span></span>
* <span data-ttu-id="dc5a9-337">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc5a9-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="dc5a9-338">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="dc5a9-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="dc5a9-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc5a9-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="dc5a9-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc5a9-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="dc5a9-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc5a9-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="dc5a9-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="dc5a9-342">AzureRM.Tags</span></span>
* <span data-ttu-id="dc5a9-343">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="dc5a9-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="dc5a9-344">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-345">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-346">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="dc5a9-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-347">Azure.Storage</span></span>
* <span data-ttu-id="dc5a9-348">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="dc5a9-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc5a9-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="dc5a9-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dc5a9-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="dc5a9-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="dc5a9-352">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="dc5a9-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="dc5a9-353">AzureRM.Automation</span></span>
* <span data-ttu-id="dc5a9-354">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-355">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-356">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dc5a9-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="dc5a9-357">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="dc5a9-358">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="dc5a9-359">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="dc5a9-360">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="dc5a9-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="dc5a9-362">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-364">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="dc5a9-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc5a9-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="dc5a9-366">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dc5a9-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-367">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-368">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dc5a9-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="dc5a9-369">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="dc5a9-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="dc5a9-370">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="dc5a9-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="dc5a9-371">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="dc5a9-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="dc5a9-372">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="dc5a9-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="dc5a9-373">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="dc5a9-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="dc5a9-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="dc5a9-374">AzureRM.Relay</span></span>
* <span data-ttu-id="dc5a9-375">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="dc5a9-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-376">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-377">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="dc5a9-378">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="dc5a9-379">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="dc5a9-380">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="dc5a9-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="dc5a9-381">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="dc5a9-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="dc5a9-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc5a9-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="dc5a9-383">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="dc5a9-384">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="dc5a9-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="dc5a9-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="dc5a9-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="dc5a9-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="dc5a9-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="dc5a9-390">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="dc5a9-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc5a9-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="dc5a9-392">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-393">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-394">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="dc5a9-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="dc5a9-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="dc5a9-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="dc5a9-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="dc5a9-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="dc5a9-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="dc5a9-397">AzureRM.Websites</span></span>
* <span data-ttu-id="dc5a9-398">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="dc5a9-399">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="dc5a9-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="dc5a9-400">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="dc5a9-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="dc5a9-401">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dc5a9-402">Ogólne</span><span class="sxs-lookup"><span data-stu-id="dc5a9-402">General</span></span>
* <span data-ttu-id="dc5a9-403">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="dc5a9-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-404">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-405">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-406">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-407">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="dc5a9-408">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="dc5a9-409">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="dc5a9-410">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="dc5a9-411">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="dc5a9-412">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="dc5a9-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="dc5a9-413">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="dc5a9-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dc5a9-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="dc5a9-415">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="dc5a9-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="dc5a9-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="dc5a9-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="dc5a9-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc5a9-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="dc5a9-420">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="dc5a9-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="dc5a9-421">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="dc5a9-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="dc5a9-422">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="dc5a9-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="dc5a9-423">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="dc5a9-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="dc5a9-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc5a9-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="dc5a9-425">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="dc5a9-426">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="dc5a9-427">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="dc5a9-428">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-430">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="dc5a9-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-431">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-432">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="dc5a9-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="dc5a9-433">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="dc5a9-434">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc5a9-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="dc5a9-435">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc5a9-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="dc5a9-436">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="dc5a9-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="dc5a9-437">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="dc5a9-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="dc5a9-438">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="dc5a9-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="dc5a9-439">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="dc5a9-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="dc5a9-440">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc5a9-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="dc5a9-441">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dc5a9-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="dc5a9-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dc5a9-443">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="dc5a9-444">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="dc5a9-445">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-446">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-447">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="dc5a9-448">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="dc5a9-449">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="dc5a9-450">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="dc5a9-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="dc5a9-451">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5a9-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="dc5a9-452">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="dc5a9-453">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="dc5a9-454">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5a9-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="dc5a9-455">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="dc5a9-456">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="dc5a9-457">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="dc5a9-458">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="dc5a9-459">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="dc5a9-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc5a9-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="dc5a9-461">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-462">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-463">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="dc5a9-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="dc5a9-464">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc5a9-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="dc5a9-465">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="dc5a9-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-466">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-467">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="dc5a9-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="dc5a9-468">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="dc5a9-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-469">Azure.Storage</span></span>
* <span data-ttu-id="dc5a9-470">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-471">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-472">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="dc5a9-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="dc5a9-473">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="dc5a9-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="dc5a9-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="dc5a9-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="dc5a9-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="dc5a9-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="dc5a9-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="dc5a9-477">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="dc5a9-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="dc5a9-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="dc5a9-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="dc5a9-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="dc5a9-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="dc5a9-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="dc5a9-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="dc5a9-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="dc5a9-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="dc5a9-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="dc5a9-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="dc5a9-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="dc5a9-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="dc5a9-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="dc5a9-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dc5a9-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="dc5a9-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="dc5a9-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="dc5a9-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="dc5a9-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="dc5a9-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="dc5a9-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="dc5a9-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="dc5a9-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="dc5a9-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="dc5a9-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="dc5a9-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="dc5a9-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="dc5a9-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dc5a9-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="dc5a9-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc5a9-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="dc5a9-498">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-500">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="dc5a9-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="dc5a9-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="dc5a9-502">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="dc5a9-503">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="dc5a9-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="dc5a9-504">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="dc5a9-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="dc5a9-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dc5a9-506">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="dc5a9-507">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-508">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-509">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="dc5a9-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="dc5a9-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dc5a9-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="dc5a9-511">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="dc5a9-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="dc5a9-512">AzureRM.Websites</span></span>
* <span data-ttu-id="dc5a9-513">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dc5a9-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="dc5a9-514">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="dc5a9-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="dc5a9-515">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="dc5a9-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="dc5a9-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="dc5a9-517">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="dc5a9-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="dc5a9-518">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="dc5a9-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-519">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-520">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="dc5a9-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-521">AzureRM.Compute</span></span>
* <span data-ttu-id="dc5a9-522">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="dc5a9-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="dc5a9-523">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="dc5a9-524">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="dc5a9-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dc5a9-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="dc5a9-526">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="dc5a9-527">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="dc5a9-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="dc5a9-528">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="dc5a9-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="dc5a9-529">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="dc5a9-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="dc5a9-530">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="dc5a9-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="dc5a9-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc5a9-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="dc5a9-532">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="dc5a9-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-533">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-534">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="dc5a9-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="dc5a9-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="dc5a9-535">AzureRM.Resources</span></span>
* <span data-ttu-id="dc5a9-536">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="dc5a9-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="dc5a9-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="dc5a9-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="dc5a9-538">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="dc5a9-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="dc5a9-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-539">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-540">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="dc5a9-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="dc5a9-541">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dc5a9-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="dc5a9-542">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dc5a9-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="dc5a9-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="dc5a9-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="dc5a9-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="dc5a9-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dc5a9-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="dc5a9-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="dc5a9-546">AzureRM.Websites</span></span>
* <span data-ttu-id="dc5a9-547">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="dc5a9-548">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="dc5a9-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="dc5a9-549">AzureRM.Profile</span></span>
* <span data-ttu-id="dc5a9-550">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="dc5a9-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="dc5a9-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc5a9-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="dc5a9-552">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="dc5a9-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc5a9-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="dc5a9-554">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dc5a9-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="dc5a9-555">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc5a9-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="dc5a9-556">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="dc5a9-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="dc5a9-557">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="dc5a9-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="dc5a9-558">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="dc5a9-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="dc5a9-559">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="dc5a9-560">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="dc5a9-560">Added support for MSI identity</span></span>
* <span data-ttu-id="dc5a9-561">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="dc5a9-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="dc5a9-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="dc5a9-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="dc5a9-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="dc5a9-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="dc5a9-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="dc5a9-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="dc5a9-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="dc5a9-566">AzureRM.Batch</span></span>
* <span data-ttu-id="dc5a9-567">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="dc5a9-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="dc5a9-568">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="dc5a9-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="dc5a9-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="dc5a9-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="dc5a9-570">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="dc5a9-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="dc5a9-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc5a9-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="dc5a9-572">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="dc5a9-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="dc5a9-573">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="dc5a9-574">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dc5a9-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="dc5a9-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="dc5a9-575">AzureRM.Network</span></span>
* <span data-ttu-id="dc5a9-576">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="dc5a9-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="dc5a9-577">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="dc5a9-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc5a9-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="dc5a9-579">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="dc5a9-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="dc5a9-581">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dc5a9-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="dc5a9-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="dc5a9-583">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="dc5a9-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="dc5a9-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc5a9-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="dc5a9-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc5a9-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="dc5a9-586">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="dc5a9-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="dc5a9-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="dc5a9-587">AzureRM.Sql</span></span>
* <span data-ttu-id="dc5a9-588">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="dc5a9-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="dc5a9-589">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="dc5a9-590">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="dc5a9-591">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="dc5a9-592">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="dc5a9-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="dc5a9-593">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dc5a9-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="dc5a9-594">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dc5a9-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="dc5a9-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="dc5a9-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="dc5a9-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="dc5a9-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="dc5a9-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dc5a9-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="dc5a9-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dc5a9-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="dc5a9-599">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
