---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383842"
---
# <a name="release-notes"></a><span data-ttu-id="6ab23-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="6ab23-103">Release notes</span></span>

<span data-ttu-id="6ab23-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="6ab23-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="6ab23-105">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6ab23-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6ab23-106">General</span></span>
* <span data-ttu-id="6ab23-107">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ab23-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6ab23-108">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="6ab23-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6ab23-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ab23-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6ab23-110">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ab23-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6ab23-111">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="6ab23-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="6ab23-112">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="6ab23-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="6ab23-113">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="6ab23-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="6ab23-114">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="6ab23-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="6ab23-115">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="6ab23-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="6ab23-116">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="6ab23-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="6ab23-117">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="6ab23-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="6ab23-118">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="6ab23-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="6ab23-119">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="6ab23-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="6ab23-120">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="6ab23-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-121">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-122">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="6ab23-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6ab23-123">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="6ab23-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6ab23-124">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ab23-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6ab23-125">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="6ab23-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-126">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-127">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="6ab23-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6ab23-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6ab23-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6ab23-129">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="6ab23-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="6ab23-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-130">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-131">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6ab23-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-133">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="6ab23-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6ab23-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ab23-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6ab23-135">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="6ab23-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6ab23-136">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="6ab23-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6ab23-137">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="6ab23-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6ab23-138">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="6ab23-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6ab23-139">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="6ab23-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6ab23-140">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="6ab23-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6ab23-141">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="6ab23-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="6ab23-142">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6ab23-143">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6ab23-143">General</span></span>
* <span data-ttu-id="6ab23-144">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ab23-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-145">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-146">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="6ab23-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-147">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-148">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="6ab23-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6ab23-149">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="6ab23-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6ab23-150">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="6ab23-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6ab23-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="6ab23-152">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="6ab23-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-153">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-154">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="6ab23-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6ab23-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6ab23-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6ab23-156">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="6ab23-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-157">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-158">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6ab23-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-160">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="6ab23-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6ab23-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ab23-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6ab23-162">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="6ab23-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6ab23-163">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="6ab23-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6ab23-164">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="6ab23-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6ab23-165">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="6ab23-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6ab23-166">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="6ab23-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6ab23-167">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="6ab23-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6ab23-168">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="6ab23-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6ab23-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6ab23-169">AzureRM.Websites</span></span>
* <span data-ttu-id="6ab23-170">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ab23-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="6ab23-171">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-172">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-173">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6ab23-174">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="6ab23-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="6ab23-175">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="6ab23-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="6ab23-176">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="6ab23-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="6ab23-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-177">Azure.Storage</span></span>
* <span data-ttu-id="6ab23-178">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="6ab23-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="6ab23-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6ab23-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6ab23-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6ab23-181">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="6ab23-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="6ab23-183">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6ab23-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ab23-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6ab23-185">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="6ab23-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6ab23-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="6ab23-187">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6ab23-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6ab23-188">AzureRM.Automation</span></span>
* <span data-ttu-id="6ab23-189">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="6ab23-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="6ab23-190">AzureRM.Backup</span></span>
* <span data-ttu-id="6ab23-191">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6ab23-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6ab23-192">AzureRM.Batch</span></span>
* <span data-ttu-id="6ab23-193">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="6ab23-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="6ab23-194">AzureRM.Billing</span></span>
* <span data-ttu-id="6ab23-195">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6ab23-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ab23-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="6ab23-197">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="6ab23-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="6ab23-199">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-200">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-201">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6ab23-202">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="6ab23-203">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6ab23-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="6ab23-204">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6ab23-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6ab23-205">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="6ab23-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6ab23-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6ab23-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="6ab23-207">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="6ab23-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ab23-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="6ab23-209">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="6ab23-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6ab23-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="6ab23-211">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="6ab23-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6ab23-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="6ab23-213">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6ab23-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6ab23-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6ab23-215">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6ab23-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6ab23-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6ab23-217">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6ab23-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ab23-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6ab23-219">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ab23-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="6ab23-220">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6ab23-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6ab23-221">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6ab23-222">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="6ab23-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6ab23-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="6ab23-224">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6ab23-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6ab23-225">AzureRM.Dns</span></span>
* <span data-ttu-id="6ab23-226">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6ab23-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ab23-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6ab23-228">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6ab23-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="6ab23-230">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="6ab23-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ab23-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="6ab23-232">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6ab23-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6ab23-233">AzureRM.Insights</span></span>
* <span data-ttu-id="6ab23-234">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6ab23-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="6ab23-236">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-238">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6ab23-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ab23-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6ab23-240">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="6ab23-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6ab23-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="6ab23-242">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="6ab23-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6ab23-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="6ab23-244">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="6ab23-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6ab23-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="6ab23-246">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="6ab23-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="6ab23-247">AzureRM.Media</span></span>
* <span data-ttu-id="6ab23-248">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-249">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-250">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6ab23-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="6ab23-251">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab23-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6ab23-252">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6ab23-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="6ab23-253">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6ab23-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6ab23-254">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6ab23-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6ab23-255">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab23-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6ab23-256">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="6ab23-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="6ab23-257">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="6ab23-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="6ab23-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6ab23-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="6ab23-259">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="6ab23-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ab23-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6ab23-261">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6ab23-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ab23-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6ab23-263">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6ab23-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6ab23-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6ab23-265">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="6ab23-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="6ab23-267">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6ab23-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6ab23-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6ab23-269">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="6ab23-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="6ab23-270">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="6ab23-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="6ab23-271">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="6ab23-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="6ab23-272">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6ab23-273">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6ab23-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="6ab23-274">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="6ab23-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6ab23-275">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="6ab23-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6ab23-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6ab23-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6ab23-277">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6ab23-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6ab23-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6ab23-279">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6ab23-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6ab23-280">AzureRM.Relay</span></span>
* <span data-ttu-id="6ab23-281">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-282">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-283">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ab23-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="6ab23-284">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ab23-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="6ab23-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="6ab23-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="6ab23-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="6ab23-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="6ab23-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="6ab23-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6ab23-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="6ab23-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6ab23-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="6ab23-292">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="6ab23-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="6ab23-293">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="6ab23-294">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6ab23-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6ab23-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6ab23-296">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-298">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6ab23-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ab23-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6ab23-300">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-301">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-302">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6ab23-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-303">AzureRM.Storage</span></span>
* <span data-ttu-id="6ab23-304">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="6ab23-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="6ab23-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="6ab23-306">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6ab23-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6ab23-307">AzureRM.Tags</span></span>
* <span data-ttu-id="6ab23-308">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6ab23-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ab23-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6ab23-310">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="6ab23-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6ab23-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="6ab23-312">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6ab23-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6ab23-313">AzureRM.Websites</span></span>
* <span data-ttu-id="6ab23-314">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="6ab23-315">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6ab23-316">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6ab23-316">General</span></span>
* <span data-ttu-id="6ab23-317">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="6ab23-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-318">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-319">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="6ab23-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="6ab23-320">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6ab23-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-321">Azure.Storage</span></span>
* <span data-ttu-id="6ab23-322">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab23-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="6ab23-323">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab23-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6ab23-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ab23-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6ab23-325">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6ab23-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6ab23-326">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="6ab23-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6ab23-327">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6ab23-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6ab23-328">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="6ab23-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6ab23-329">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6ab23-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6ab23-330">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="6ab23-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-331">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-332">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="6ab23-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6ab23-333">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6ab23-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6ab23-334">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ab23-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6ab23-335">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="6ab23-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6ab23-336">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="6ab23-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6ab23-337">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="6ab23-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6ab23-338">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6ab23-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6ab23-339">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="6ab23-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6ab23-340">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6ab23-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6ab23-341">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="6ab23-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6ab23-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6ab23-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6ab23-343">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6ab23-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6ab23-344">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="6ab23-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6ab23-345">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6ab23-346">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6ab23-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6ab23-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ab23-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6ab23-348">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="6ab23-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6ab23-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="6ab23-350">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="6ab23-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6ab23-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6ab23-351">AzureRM.Insights</span></span>
* <span data-ttu-id="6ab23-352">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="6ab23-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6ab23-353">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="6ab23-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-355">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ab23-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-356">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-357">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="6ab23-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-358">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-359">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6ab23-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6ab23-360">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6ab23-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-362">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="6ab23-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6ab23-363">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="6ab23-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-364">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-365">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ab23-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6ab23-366">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ab23-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6ab23-367">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ab23-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6ab23-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6ab23-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6ab23-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6ab23-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6ab23-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6ab23-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6ab23-371">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ab23-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6ab23-372">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6ab23-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6ab23-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-373">AzureRM.Storage</span></span>
* <span data-ttu-id="6ab23-374">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ab23-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6ab23-375">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="6ab23-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6ab23-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ab23-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6ab23-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ab23-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6ab23-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ab23-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6ab23-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6ab23-379">AzureRM.Tags</span></span>
* <span data-ttu-id="6ab23-380">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="6ab23-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6ab23-381">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-382">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-383">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="6ab23-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6ab23-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-384">Azure.Storage</span></span>
* <span data-ttu-id="6ab23-385">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="6ab23-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6ab23-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ab23-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6ab23-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ab23-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6ab23-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6ab23-389">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="6ab23-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6ab23-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6ab23-390">AzureRM.Automation</span></span>
* <span data-ttu-id="6ab23-391">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="6ab23-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-392">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-393">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ab23-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6ab23-394">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="6ab23-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6ab23-395">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="6ab23-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6ab23-396">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="6ab23-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6ab23-397">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="6ab23-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6ab23-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="6ab23-399">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="6ab23-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-401">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ab23-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6ab23-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ab23-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6ab23-403">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ab23-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-404">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-405">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6ab23-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6ab23-406">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6ab23-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6ab23-407">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="6ab23-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6ab23-408">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6ab23-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6ab23-409">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6ab23-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6ab23-410">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="6ab23-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6ab23-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6ab23-411">AzureRM.Relay</span></span>
* <span data-ttu-id="6ab23-412">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="6ab23-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-413">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-414">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="6ab23-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6ab23-415">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6ab23-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6ab23-416">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ab23-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6ab23-417">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6ab23-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6ab23-418">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="6ab23-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-420">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="6ab23-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6ab23-421">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="6ab23-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6ab23-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6ab23-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6ab23-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6ab23-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6ab23-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6ab23-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6ab23-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6ab23-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6ab23-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6ab23-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6ab23-427">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="6ab23-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6ab23-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ab23-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6ab23-429">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="6ab23-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-430">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-431">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="6ab23-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6ab23-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6ab23-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6ab23-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6ab23-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6ab23-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6ab23-434">AzureRM.Websites</span></span>
* <span data-ttu-id="6ab23-435">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="6ab23-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6ab23-436">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="6ab23-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6ab23-437">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="6ab23-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6ab23-438">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6ab23-439">Ogólne</span><span class="sxs-lookup"><span data-stu-id="6ab23-439">General</span></span>
* <span data-ttu-id="6ab23-440">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="6ab23-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-441">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-442">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="6ab23-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-443">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-444">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6ab23-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6ab23-445">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="6ab23-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6ab23-446">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6ab23-447">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6ab23-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6ab23-448">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6ab23-449">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="6ab23-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6ab23-450">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6ab23-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6ab23-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6ab23-452">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="6ab23-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6ab23-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6ab23-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6ab23-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6ab23-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ab23-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6ab23-457">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6ab23-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6ab23-458">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6ab23-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6ab23-459">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="6ab23-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6ab23-460">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="6ab23-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6ab23-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ab23-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="6ab23-462">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6ab23-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6ab23-463">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="6ab23-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6ab23-464">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="6ab23-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6ab23-465">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6ab23-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-467">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6ab23-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-468">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-469">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6ab23-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6ab23-470">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="6ab23-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6ab23-471">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6ab23-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6ab23-472">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6ab23-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6ab23-473">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6ab23-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6ab23-474">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6ab23-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6ab23-475">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6ab23-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6ab23-476">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6ab23-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6ab23-477">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ab23-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6ab23-478">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6ab23-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6ab23-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6ab23-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6ab23-480">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="6ab23-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6ab23-481">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ab23-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6ab23-482">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="6ab23-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-483">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-484">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="6ab23-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6ab23-485">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6ab23-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6ab23-486">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6ab23-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6ab23-487">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="6ab23-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6ab23-488">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab23-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6ab23-489">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6ab23-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6ab23-490">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6ab23-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6ab23-491">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab23-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6ab23-492">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6ab23-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6ab23-493">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6ab23-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6ab23-494">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="6ab23-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6ab23-495">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="6ab23-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6ab23-496">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="6ab23-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6ab23-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ab23-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6ab23-498">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6ab23-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-499">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-500">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6ab23-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6ab23-501">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ab23-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6ab23-502">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6ab23-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-503">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-504">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="6ab23-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6ab23-505">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="6ab23-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6ab23-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6ab23-506">Azure.Storage</span></span>
* <span data-ttu-id="6ab23-507">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="6ab23-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-508">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-509">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="6ab23-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6ab23-510">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ab23-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6ab23-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6ab23-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6ab23-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6ab23-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6ab23-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6ab23-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6ab23-514">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="6ab23-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6ab23-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6ab23-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6ab23-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6ab23-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6ab23-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6ab23-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6ab23-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6ab23-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6ab23-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="6ab23-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6ab23-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6ab23-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ab23-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6ab23-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ab23-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6ab23-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6ab23-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6ab23-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6ab23-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ab23-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6ab23-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6ab23-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6ab23-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6ab23-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6ab23-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6ab23-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6ab23-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6ab23-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6ab23-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6ab23-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6ab23-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6ab23-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6ab23-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ab23-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6ab23-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ab23-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6ab23-535">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="6ab23-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-537">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6ab23-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6ab23-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ab23-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6ab23-539">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="6ab23-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6ab23-540">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="6ab23-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6ab23-541">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6ab23-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6ab23-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6ab23-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6ab23-543">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="6ab23-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6ab23-544">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6ab23-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-545">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-546">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6ab23-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6ab23-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ab23-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6ab23-548">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6ab23-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6ab23-549">AzureRM.Websites</span></span>
* <span data-ttu-id="6ab23-550">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab23-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6ab23-551">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="6ab23-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6ab23-552">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6ab23-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6ab23-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ab23-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6ab23-554">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="6ab23-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6ab23-555">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="6ab23-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-556">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-557">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="6ab23-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6ab23-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6ab23-558">AzureRM.Compute</span></span>
* <span data-ttu-id="6ab23-559">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="6ab23-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6ab23-560">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="6ab23-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6ab23-561">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="6ab23-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6ab23-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6ab23-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6ab23-563">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="6ab23-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6ab23-564">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="6ab23-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6ab23-565">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="6ab23-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6ab23-566">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="6ab23-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6ab23-567">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="6ab23-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6ab23-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ab23-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6ab23-569">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="6ab23-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-570">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-571">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="6ab23-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6ab23-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6ab23-572">AzureRM.Resources</span></span>
* <span data-ttu-id="6ab23-573">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="6ab23-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6ab23-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6ab23-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6ab23-575">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="6ab23-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6ab23-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-576">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-577">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="6ab23-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6ab23-578">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6ab23-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6ab23-579">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6ab23-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6ab23-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6ab23-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6ab23-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ab23-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6ab23-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6ab23-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6ab23-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6ab23-583">AzureRM.Websites</span></span>
* <span data-ttu-id="6ab23-584">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="6ab23-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6ab23-585">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="6ab23-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6ab23-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6ab23-586">AzureRM.Profile</span></span>
* <span data-ttu-id="6ab23-587">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="6ab23-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6ab23-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ab23-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6ab23-589">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="6ab23-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6ab23-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ab23-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6ab23-591">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6ab23-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6ab23-592">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ab23-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6ab23-593">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="6ab23-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6ab23-594">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="6ab23-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6ab23-595">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="6ab23-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6ab23-596">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="6ab23-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6ab23-597">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="6ab23-597">Added support for MSI identity</span></span>
* <span data-ttu-id="6ab23-598">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="6ab23-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6ab23-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6ab23-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6ab23-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab23-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6ab23-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6ab23-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6ab23-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6ab23-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6ab23-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6ab23-603">AzureRM.Batch</span></span>
* <span data-ttu-id="6ab23-604">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6ab23-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6ab23-605">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6ab23-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6ab23-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6ab23-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="6ab23-607">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="6ab23-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6ab23-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ab23-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6ab23-609">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6ab23-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6ab23-610">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6ab23-611">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6ab23-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6ab23-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6ab23-612">AzureRM.Network</span></span>
* <span data-ttu-id="6ab23-613">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6ab23-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6ab23-614">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="6ab23-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6ab23-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab23-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6ab23-616">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6ab23-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6ab23-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6ab23-618">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6ab23-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6ab23-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6ab23-620">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="6ab23-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6ab23-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6ab23-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6ab23-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ab23-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6ab23-623">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="6ab23-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6ab23-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6ab23-624">AzureRM.Sql</span></span>
* <span data-ttu-id="6ab23-625">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="6ab23-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6ab23-626">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="6ab23-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6ab23-627">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="6ab23-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6ab23-628">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="6ab23-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6ab23-629">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="6ab23-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6ab23-630">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6ab23-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6ab23-631">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6ab23-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6ab23-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6ab23-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6ab23-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ab23-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6ab23-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6ab23-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6ab23-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ab23-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6ab23-636">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="6ab23-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
