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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106755"
---
# <a name="release-notes"></a><span data-ttu-id="f9b70-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="f9b70-103">Release notes</span></span>

<span data-ttu-id="f9b70-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="f9b70-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="f9b70-105">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f9b70-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-106">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-107">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9b70-108">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="f9b70-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="f9b70-109">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="f9b70-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="f9b70-110">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="f9b70-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="f9b70-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-111">Azure.Storage</span></span>
* <span data-ttu-id="f9b70-112">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="f9b70-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="f9b70-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f9b70-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9b70-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9b70-115">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="f9b70-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="f9b70-117">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9b70-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b70-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9b70-119">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="f9b70-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9b70-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="f9b70-121">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f9b70-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9b70-122">AzureRM.Automation</span></span>
* <span data-ttu-id="f9b70-123">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="f9b70-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f9b70-124">AzureRM.Backup</span></span>
* <span data-ttu-id="f9b70-125">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f9b70-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f9b70-126">AzureRM.Batch</span></span>
* <span data-ttu-id="f9b70-127">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="f9b70-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="f9b70-128">AzureRM.Billing</span></span>
* <span data-ttu-id="f9b70-129">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f9b70-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9b70-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="f9b70-131">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f9b70-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f9b70-133">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-134">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-135">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9b70-136">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="f9b70-137">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f9b70-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="f9b70-138">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f9b70-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f9b70-139">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="f9b70-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f9b70-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f9b70-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="f9b70-141">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="f9b70-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9b70-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="f9b70-143">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="f9b70-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9b70-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="f9b70-145">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="f9b70-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f9b70-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="f9b70-147">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9b70-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9b70-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9b70-149">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f9b70-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9b70-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f9b70-151">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9b70-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9b70-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9b70-153">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9b70-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="f9b70-154">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f9b70-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f9b70-155">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9b70-156">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="f9b70-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f9b70-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="f9b70-158">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f9b70-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f9b70-159">AzureRM.Dns</span></span>
* <span data-ttu-id="f9b70-160">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f9b70-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9b70-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f9b70-162">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9b70-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9b70-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9b70-164">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="f9b70-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9b70-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="f9b70-166">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9b70-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9b70-167">AzureRM.Insights</span></span>
* <span data-ttu-id="f9b70-168">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f9b70-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9b70-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="f9b70-170">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-172">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f9b70-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9b70-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f9b70-174">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="f9b70-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9b70-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="f9b70-176">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="f9b70-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f9b70-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="f9b70-178">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="f9b70-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9b70-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9b70-180">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="f9b70-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="f9b70-181">AzureRM.Media</span></span>
* <span data-ttu-id="f9b70-182">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-183">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-184">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9b70-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="f9b70-185">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9b70-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9b70-186">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9b70-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="f9b70-187">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f9b70-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f9b70-188">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f9b70-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f9b70-189">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9b70-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9b70-190">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="f9b70-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="f9b70-191">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="f9b70-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="f9b70-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f9b70-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="f9b70-193">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="f9b70-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9b70-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f9b70-195">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f9b70-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9b70-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f9b70-197">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f9b70-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9b70-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9b70-199">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="f9b70-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="f9b70-201">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9b70-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9b70-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9b70-203">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="f9b70-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="f9b70-204">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="f9b70-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="f9b70-205">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="f9b70-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="f9b70-206">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9b70-207">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f9b70-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="f9b70-208">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="f9b70-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="f9b70-209">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="f9b70-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f9b70-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9b70-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9b70-211">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f9b70-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9b70-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f9b70-213">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f9b70-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f9b70-214">AzureRM.Relay</span></span>
* <span data-ttu-id="f9b70-215">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9b70-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9b70-216">AzureRM.Resources</span></span>
* <span data-ttu-id="f9b70-217">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f9b70-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="f9b70-218">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9b70-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="f9b70-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9b70-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9b70-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9b70-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9b70-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9b70-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f9b70-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="f9b70-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f9b70-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="f9b70-226">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="f9b70-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="f9b70-227">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="f9b70-228">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f9b70-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f9b70-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f9b70-230">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9b70-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9b70-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9b70-232">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9b70-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9b70-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9b70-234">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-235">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-236">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9b70-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-237">AzureRM.Storage</span></span>
* <span data-ttu-id="f9b70-238">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="f9b70-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9b70-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="f9b70-240">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f9b70-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f9b70-241">AzureRM.Tags</span></span>
* <span data-ttu-id="f9b70-242">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9b70-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9b70-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9b70-244">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="f9b70-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f9b70-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="f9b70-246">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9b70-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9b70-247">AzureRM.Websites</span></span>
* <span data-ttu-id="f9b70-248">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="f9b70-249">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f9b70-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9b70-250">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f9b70-250">General</span></span>
* <span data-ttu-id="f9b70-251">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="f9b70-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-252">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-253">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="f9b70-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="f9b70-254">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9b70-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-255">Azure.Storage</span></span>
* <span data-ttu-id="f9b70-256">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b70-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="f9b70-257">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b70-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9b70-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b70-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9b70-259">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="f9b70-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="f9b70-260">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="f9b70-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="f9b70-261">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="f9b70-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="f9b70-262">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="f9b70-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="f9b70-263">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="f9b70-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="f9b70-264">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="f9b70-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-265">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-266">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="f9b70-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="f9b70-267">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f9b70-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="f9b70-268">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f9b70-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="f9b70-269">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="f9b70-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="f9b70-270">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f9b70-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="f9b70-271">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="f9b70-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="f9b70-272">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f9b70-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="f9b70-273">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="f9b70-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="f9b70-274">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f9b70-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="f9b70-275">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="f9b70-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9b70-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9b70-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9b70-277">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="f9b70-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="f9b70-278">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="f9b70-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="f9b70-279">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="f9b70-280">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f9b70-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9b70-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9b70-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9b70-282">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="f9b70-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9b70-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9b70-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9b70-284">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="f9b70-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9b70-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9b70-285">AzureRM.Insights</span></span>
* <span data-ttu-id="f9b70-286">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="f9b70-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="f9b70-287">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="f9b70-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-289">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f9b70-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-290">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-291">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="f9b70-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9b70-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9b70-292">AzureRM.Resources</span></span>
* <span data-ttu-id="f9b70-293">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f9b70-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="f9b70-294">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f9b70-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9b70-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9b70-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9b70-296">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="f9b70-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="f9b70-297">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="f9b70-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-298">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-299">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9b70-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="f9b70-300">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9b70-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f9b70-301">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9b70-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="f9b70-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="f9b70-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="f9b70-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="f9b70-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="f9b70-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="f9b70-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="f9b70-305">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f9b70-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="f9b70-306">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="f9b70-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9b70-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-307">AzureRM.Storage</span></span>
* <span data-ttu-id="f9b70-308">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9b70-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="f9b70-309">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="f9b70-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="f9b70-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9b70-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f9b70-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9b70-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f9b70-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9b70-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f9b70-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f9b70-313">AzureRM.Tags</span></span>
* <span data-ttu-id="f9b70-314">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="f9b70-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="f9b70-315">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f9b70-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-316">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-317">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="f9b70-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9b70-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-318">Azure.Storage</span></span>
* <span data-ttu-id="f9b70-319">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="f9b70-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="f9b70-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9b70-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="f9b70-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9b70-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9b70-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9b70-323">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="f9b70-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f9b70-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9b70-324">AzureRM.Automation</span></span>
* <span data-ttu-id="f9b70-325">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="f9b70-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-326">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-327">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f9b70-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="f9b70-328">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="f9b70-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f9b70-329">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="f9b70-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f9b70-330">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="f9b70-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="f9b70-331">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="f9b70-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9b70-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9b70-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9b70-333">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="f9b70-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-335">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f9b70-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f9b70-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9b70-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f9b70-337">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f9b70-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-338">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-339">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f9b70-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="f9b70-340">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f9b70-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="f9b70-341">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="f9b70-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="f9b70-342">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f9b70-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="f9b70-343">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f9b70-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="f9b70-344">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="f9b70-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f9b70-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f9b70-345">AzureRM.Relay</span></span>
* <span data-ttu-id="f9b70-346">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="f9b70-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9b70-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9b70-347">AzureRM.Resources</span></span>
* <span data-ttu-id="f9b70-348">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="f9b70-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="f9b70-349">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="f9b70-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="f9b70-350">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f9b70-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="f9b70-351">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="f9b70-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="f9b70-352">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="f9b70-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9b70-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9b70-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9b70-354">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="f9b70-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="f9b70-355">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="f9b70-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="f9b70-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9b70-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9b70-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9b70-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9b70-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9b70-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9b70-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9b70-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9b70-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9b70-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="f9b70-361">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="f9b70-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9b70-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9b70-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9b70-363">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="f9b70-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-364">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-365">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="f9b70-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="f9b70-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b70-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="f9b70-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b70-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9b70-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9b70-368">AzureRM.Websites</span></span>
* <span data-ttu-id="f9b70-369">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="f9b70-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="f9b70-370">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="f9b70-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="f9b70-371">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="f9b70-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="f9b70-372">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f9b70-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9b70-373">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f9b70-373">General</span></span>
* <span data-ttu-id="f9b70-374">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="f9b70-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-375">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-376">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="f9b70-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-377">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-378">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f9b70-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="f9b70-379">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="f9b70-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="f9b70-380">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f9b70-381">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f9b70-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="f9b70-382">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="f9b70-383">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f9b70-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="f9b70-384">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f9b70-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9b70-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f9b70-386">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="f9b70-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="f9b70-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f9b70-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f9b70-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9b70-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9b70-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9b70-391">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f9b70-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f9b70-392">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f9b70-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f9b70-393">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="f9b70-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="f9b70-394">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="f9b70-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9b70-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9b70-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9b70-396">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f9b70-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="f9b70-397">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="f9b70-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="f9b70-398">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="f9b70-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="f9b70-399">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f9b70-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-401">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f9b70-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-402">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-403">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f9b70-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="f9b70-404">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="f9b70-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="f9b70-405">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f9b70-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f9b70-406">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f9b70-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f9b70-407">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f9b70-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9b70-408">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f9b70-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9b70-409">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f9b70-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9b70-410">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f9b70-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f9b70-411">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9b70-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f9b70-412">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9b70-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9b70-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9b70-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9b70-414">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="f9b70-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="f9b70-415">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f9b70-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="f9b70-416">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="f9b70-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9b70-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9b70-417">AzureRM.Resources</span></span>
* <span data-ttu-id="f9b70-418">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="f9b70-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="f9b70-419">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f9b70-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="f9b70-420">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f9b70-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="f9b70-421">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="f9b70-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="f9b70-422">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f9b70-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="f9b70-423">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f9b70-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f9b70-424">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f9b70-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f9b70-425">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f9b70-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="f9b70-426">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f9b70-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f9b70-427">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f9b70-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f9b70-428">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f9b70-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="f9b70-429">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="f9b70-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="f9b70-430">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="f9b70-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="f9b70-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9b70-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9b70-432">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f9b70-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-433">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-434">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f9b70-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="f9b70-435">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9b70-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="f9b70-436">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f9b70-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-437">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-438">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="f9b70-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f9b70-439">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="f9b70-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9b70-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9b70-440">Azure.Storage</span></span>
* <span data-ttu-id="f9b70-441">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="f9b70-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-442">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-443">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="f9b70-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f9b70-444">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9b70-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f9b70-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f9b70-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f9b70-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f9b70-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f9b70-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f9b70-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f9b70-448">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="f9b70-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f9b70-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9b70-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f9b70-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9b70-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f9b70-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9b70-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f9b70-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9b70-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f9b70-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f9b70-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f9b70-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f9b70-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f9b70-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f9b70-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f9b70-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f9b70-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f9b70-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f9b70-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f9b70-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9b70-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f9b70-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f9b70-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f9b70-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f9b70-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f9b70-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f9b70-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f9b70-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f9b70-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f9b70-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f9b70-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f9b70-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f9b70-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f9b70-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f9b70-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f9b70-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9b70-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f9b70-469">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="f9b70-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-471">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f9b70-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f9b70-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9b70-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f9b70-473">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="f9b70-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f9b70-474">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="f9b70-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f9b70-475">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="f9b70-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9b70-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9b70-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9b70-477">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="f9b70-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f9b70-478">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="f9b70-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-479">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-480">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f9b70-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9b70-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9b70-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9b70-482">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9b70-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9b70-483">AzureRM.Websites</span></span>
* <span data-ttu-id="f9b70-484">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f9b70-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f9b70-485">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="f9b70-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f9b70-486">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f9b70-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f9b70-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9b70-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f9b70-488">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="f9b70-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f9b70-489">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f9b70-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-490">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-491">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="f9b70-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9b70-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9b70-492">AzureRM.Compute</span></span>
* <span data-ttu-id="f9b70-493">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="f9b70-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f9b70-494">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="f9b70-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f9b70-495">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="f9b70-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9b70-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9b70-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9b70-497">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="f9b70-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f9b70-498">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="f9b70-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f9b70-499">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="f9b70-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f9b70-500">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="f9b70-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f9b70-501">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="f9b70-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f9b70-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b70-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9b70-503">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="f9b70-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-504">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-505">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="f9b70-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9b70-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9b70-506">AzureRM.Resources</span></span>
* <span data-ttu-id="f9b70-507">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f9b70-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f9b70-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f9b70-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f9b70-509">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="f9b70-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f9b70-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-510">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-511">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="f9b70-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f9b70-512">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9b70-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f9b70-513">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9b70-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f9b70-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f9b70-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f9b70-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f9b70-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f9b70-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9b70-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9b70-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9b70-517">AzureRM.Websites</span></span>
* <span data-ttu-id="f9b70-518">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="f9b70-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f9b70-519">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f9b70-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9b70-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9b70-520">AzureRM.Profile</span></span>
* <span data-ttu-id="f9b70-521">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="f9b70-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9b70-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9b70-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9b70-523">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="f9b70-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9b70-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b70-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9b70-525">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f9b70-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f9b70-526">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9b70-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f9b70-527">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="f9b70-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f9b70-528">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="f9b70-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f9b70-529">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="f9b70-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f9b70-530">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="f9b70-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f9b70-531">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="f9b70-531">Added support for MSI identity</span></span>
* <span data-ttu-id="f9b70-532">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="f9b70-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f9b70-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b70-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f9b70-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b70-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f9b70-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f9b70-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f9b70-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f9b70-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f9b70-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f9b70-537">AzureRM.Batch</span></span>
* <span data-ttu-id="f9b70-538">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="f9b70-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f9b70-539">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="f9b70-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f9b70-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f9b70-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="f9b70-541">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="f9b70-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9b70-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9b70-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9b70-543">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f9b70-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f9b70-544">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f9b70-545">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9b70-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f9b70-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9b70-546">AzureRM.Network</span></span>
* <span data-ttu-id="f9b70-547">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="f9b70-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f9b70-548">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="f9b70-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f9b70-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b70-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f9b70-550">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f9b70-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f9b70-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9b70-552">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f9b70-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f9b70-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9b70-554">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="f9b70-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f9b70-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9b70-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9b70-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9b70-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9b70-557">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="f9b70-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9b70-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9b70-558">AzureRM.Sql</span></span>
* <span data-ttu-id="f9b70-559">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f9b70-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f9b70-560">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="f9b70-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f9b70-561">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="f9b70-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f9b70-562">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="f9b70-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f9b70-563">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="f9b70-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f9b70-564">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9b70-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f9b70-565">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9b70-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f9b70-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f9b70-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f9b70-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f9b70-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f9b70-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9b70-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9b70-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9b70-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9b70-570">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="f9b70-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
