---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080202"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="19174-103">Informacje o wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="19174-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="19174-104">3.8.0 — kwiecień 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="19174-105">Najważniejsze zmiany od ostatniej wersji</span><span class="sxs-lookup"><span data-stu-id="19174-105">Highlights since the last release</span></span>
* <span data-ttu-id="19174-106">Wersje programu PowerShell obsługiwane przez bibliotekę Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="19174-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-107">Az.Accounts</span></span>
* <span data-ttu-id="19174-108">Zaktualizowano adres URL ankiety Azure PowerShell w poleceniu „Resolve-AzError” [nr 11507]</span><span class="sxs-lookup"><span data-stu-id="19174-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-109">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-110">Dodano powiadomienie o zmianie powodującej niezgodność dotyczącej danych wyjściowych poleceń cmdlet dla plików platformy Azure, która zostanie wprowadzona w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="19174-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="19174-111">Zaktualizowano dokumentację polecenia „Set-AzApiManagementGroup” w celu określenia parametru GroupId</span><span class="sxs-lookup"><span data-stu-id="19174-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-112">Az.Cdn</span></span>
* <span data-ttu-id="19174-113">Poprawiono wyświetlanie jednostek SKU z cenami dotyczącymi sieci ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="19174-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-115">Dodano obsługę elementów Identity, Encryption i UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="19174-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-116">Az.Compute</span></span>
* <span data-ttu-id="19174-117">Dodano polecenie cmdlet „Set-AzVmssOrchestrationServiceState”.</span><span class="sxs-lookup"><span data-stu-id="19174-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="19174-118">Polecenie „Get-AzVmss” z parametrem -InstanceView wyświetla stany OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="19174-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-119">Az.IotHub</span></span>
* <span data-ttu-id="19174-120">Nowe polecenia cmdlet do zarządzania konfiguracją bliźniaczej reprezentacji urządzenia IoT:</span><span class="sxs-lookup"><span data-stu-id="19174-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="19174-121">„Get-AzIotHubDeviceTwin”</span><span class="sxs-lookup"><span data-stu-id="19174-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="19174-122">„Update-AzIotHubDeviceTwin”</span><span class="sxs-lookup"><span data-stu-id="19174-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="19174-123">Dodano polecenie cmdlet do wywoływania metody bezpośredniej na urządzeniu w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="19174-124">Nowe polecenia cmdlet do zarządzania konfiguracją bliźniaczej reprezentacji modułu urządzenia IoT:</span><span class="sxs-lookup"><span data-stu-id="19174-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="19174-125">„Get-AzIotHubModuleTwin”</span><span class="sxs-lookup"><span data-stu-id="19174-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="19174-126">„Update-AzIotHubModuleTwin”</span><span class="sxs-lookup"><span data-stu-id="19174-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="19174-127">Zarządzanie konfiguracją automatycznego zarządzania urządzeniami IoT na dużą skalę.</span><span class="sxs-lookup"><span data-stu-id="19174-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="19174-128">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-128">New cmdlets are:</span></span>
    - <span data-ttu-id="19174-129">„Add-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="19174-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="19174-130">„Get-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="19174-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="19174-131">„Remove-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="19174-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="19174-132">„Set-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="19174-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="19174-133">Dodano polecenie cmdlet do wywołania metody modułu brzegowego w centrum IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="19174-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-134">Az.KeyVault</span></span>
* <span data-ttu-id="19174-135">Dodano nowe polecenie cmdlet „Update-AzKeyVault”, które umożliwia włączenie usuwania nietrwałego i ochrony przed oczyszczeniem w magazynie</span><span class="sxs-lookup"><span data-stu-id="19174-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="19174-136">Dodano obsługę do modułu Microsoft.PowerShell.SecretManagement [nr 11178]</span><span class="sxs-lookup"><span data-stu-id="19174-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="19174-137">Usunięto błąd w przykładach polecenia „Remove-AzKeyVaultManagedStorageSasDefinition” [nr 11479]</span><span class="sxs-lookup"><span data-stu-id="19174-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="19174-138">Dodano obsługę do prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="19174-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="19174-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="19174-139">Az.Maintenance</span></span>
* <span data-ttu-id="19174-140">Publikowanie ogólnie dostępnej wersji poleceń cmdlet modułu Maintenance</span><span class="sxs-lookup"><span data-stu-id="19174-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-141">Az.Monitor</span></span>
* <span data-ttu-id="19174-142">Dodano polecenia cmdlet dla zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="19174-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="19174-143">„Get-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="19174-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="19174-144">„Remove-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="19174-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="19174-145">„New-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="19174-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="19174-146">„Update-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="19174-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="19174-147">„Get-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="19174-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="19174-148">„New-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="19174-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="19174-149">„Remove-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="19174-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-150">Az.Network</span></span>
* <span data-ttu-id="19174-151">Zaktualizowano polecenia cmdlet, aby umożliwić połączenie przy użyciu prywatnego adresu IP dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="19174-152">„New-AzVirtualNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="19174-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="19174-153">„Set-AzVirtualNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="19174-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="19174-154">„New-AzVirtualNetworkGatewayConnection”</span><span class="sxs-lookup"><span data-stu-id="19174-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="19174-155">„Set-AzVirtualNetworkGatewayConnection”</span><span class="sxs-lookup"><span data-stu-id="19174-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="19174-156">Zaktualizowano polecenia cmdlet, aby umożliwić używanie elementów LocalNetworkGateways i VpnSites opartych na nazwach FQDN</span><span class="sxs-lookup"><span data-stu-id="19174-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="19174-157">„New-AzLocalNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="19174-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="19174-158">„New-AzVpnSiteLink”</span><span class="sxs-lookup"><span data-stu-id="19174-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="19174-159">Dodano obsługę rodziny adresów IPv6 w elemencie ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="19174-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="19174-160">Dodano polecenie „Set-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="19174-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="19174-161">Pozwala na ustawianie wszystkich istniejących właściwości, w tym IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="19174-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="19174-162">Zaktualizowano polecenie „Add-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="19174-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="19174-163">Dodano kolejny opcjonalny parametr AddressPrefixType umożliwiający określenie rodziny adresów prefiksu adresu</span><span class="sxs-lookup"><span data-stu-id="19174-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="19174-164">Zaktualizowano polecenia cmdlet, aby umożliwić ustawianie limitu czasu wykrywania nieaktywnych elementów równorzędnych w połączeniach bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="19174-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="19174-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="19174-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="19174-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-168">Dodano polecenie cmdlet „Start-AzPolicyComplianceScan” na potrzeby wyzwalania skanowania pod kątem zgodności z zasadami</span><span class="sxs-lookup"><span data-stu-id="19174-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="19174-169">Dodano definicję zasad, definicję zestawu i wersje przypisania do danych wyjściowych polecenia „Get-AzPolicyState”</span><span class="sxs-lookup"><span data-stu-id="19174-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-171">Poprawiono formatowanie kodu i użyteczność przykładów polecenia „New-AzServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="19174-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-172">Az.Sql</span></span>
* <span data-ttu-id="19174-173">Dodano polecenia cmdlet „Get-AzSqlInstanceOperation” i „Stop-AzSqlInstanceOperation”</span><span class="sxs-lookup"><span data-stu-id="19174-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="19174-174">Dodano obsługę inspekcji do konta magazynu w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-175">Az.Storage</span></span>
* <span data-ttu-id="19174-176">Dodano powiadomienie o zmianie powodującej niezgodność dotyczącej danych wyjściowych poleceń cmdlet dla plików platformy Azure, która zostanie wprowadzona w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="19174-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="19174-177">Dodano obsługę nowych wartości SkuName (StandardGZRS i StandardRAGZRS) podczas tworzenia/aktualizowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="19174-178">„New-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="19174-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="19174-179">„Set-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="19174-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="19174-180">Dodano obsługę usługi Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="19174-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="19174-181">„New-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="19174-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="19174-182">„Get-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="19174-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="19174-183">„Get-AzDataLakeGen2ChildItem”</span><span class="sxs-lookup"><span data-stu-id="19174-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="19174-184">„Move-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="19174-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="19174-185">„Set-AzDataLakeGen2ItemAclObject”</span><span class="sxs-lookup"><span data-stu-id="19174-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="19174-186">„Update-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="19174-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="19174-187">„Get-AzDataLakeGen2ItemContent”</span><span class="sxs-lookup"><span data-stu-id="19174-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="19174-188">„Remove-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="19174-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="19174-189">0.10.0-preview — kwiecień 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="19174-190">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-190">General</span></span>
* <span data-ttu-id="19174-191">Moduły Az są teraz dostępne w wersji zapoznawczej w usłudze Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="19174-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="19174-192">Pozwala to na uzyskanie zgodności między wieloma platformami w przypadku systemów Linux i macOS.</span><span class="sxs-lookup"><span data-stu-id="19174-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="19174-193">Usługa Azure Stack Hub obsługuje teraz program PowerShell Core z modułami Az; więcej informacji znajduje się [tutaj](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="19174-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="19174-194">Moduły Az obsługują profil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="19174-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="19174-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="19174-195">Az.Billing</span></span>
  - <span data-ttu-id="19174-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-196">Az.Compute</span></span>
  - <span data-ttu-id="19174-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="19174-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="19174-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-198">Az.EventHub</span></span>
  - <span data-ttu-id="19174-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-199">Az.IotHub</span></span>
  - <span data-ttu-id="19174-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-200">Az.KeyVault</span></span>
  - <span data-ttu-id="19174-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-201">Az.Monitor</span></span>
  - <span data-ttu-id="19174-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-202">Az.Network</span></span>
  - <span data-ttu-id="19174-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-203">Az.Resources</span></span>
  - <span data-ttu-id="19174-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-204">Az.Storage</span></span>
  - <span data-ttu-id="19174-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-205">Az.Websites</span></span>
* <span data-ttu-id="19174-206">Wprowadzono trzy nowe moduły programu PowerShell dla modułu Az, które działają w usłudze Azure Stack Hub: Az.Databox, Az.IotHub i Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="19174-207">Polecenia pozostają w zasadzie takie same, wprowadzono tylko niewielkie zmiany, np. zmieniono ciąg AzureRM na Az</span><span class="sxs-lookup"><span data-stu-id="19174-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="19174-208">Zaktualizowany link do dokumentacji programu PowerShell dla usługi Azure Stack Hub można znaleźć [tutaj](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="19174-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="19174-209">3.7.0 — marzec 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-210">Az.Accounts</span></span>
* <span data-ttu-id="19174-211">Rozwiązano problem powodujący zgłaszanie wyjątku NullReferenceException przez polecenia „Get-AzTenant”, „Get-AzDefault” i „Set-AzDefault”, gdy użytkownik nie jest zalogowany [nr 10292]</span><span class="sxs-lookup"><span data-stu-id="19174-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-212">Az.Compute</span></span>
* <span data-ttu-id="19174-213">Dodano następujące parametry do polecenia cmdlet „New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="19174-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="19174-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="19174-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="19174-215">Zezwolono na właściwość Encryption parametru Target polecenia cmdlet „New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="19174-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="19174-216">Rozwiązano problem tempDisk w przypadku poleceń cmdlet „Set-AzVmss” z parametrem -Reimage i „Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="19174-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="19174-217">[nr 11354]</span><span class="sxs-lookup"><span data-stu-id="19174-217">[#11354]</span></span>
* <span data-ttu-id="19174-218">Do poniższych poleceń cmdlet dodano obsługę nowego rozszerzenia SAP</span><span class="sxs-lookup"><span data-stu-id="19174-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="19174-219">„Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="19174-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="19174-220">„Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="19174-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="19174-221">„Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="19174-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="19174-222">„Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="19174-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="19174-223">Usunięto błędy w przykładach dokumentu pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="19174-224">Pokazano dokładną wartość ciągu dla parametru PowerState maszyny wirtualnej w formacie tabeli.</span><span class="sxs-lookup"><span data-stu-id="19174-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="19174-225">„New-AzVmssConfig”: poprawiono serializację właściwości AutomaticRepairs, gdy właściwość SinglePlacementGroup jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="19174-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="19174-226">[nr 11257]</span><span class="sxs-lookup"><span data-stu-id="19174-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-227">Az.DataFactory</span></span>
* <span data-ttu-id="19174-228">Zaktualizowano wersję zestawu ADF .Net SDK do 4.8.0</span><span class="sxs-lookup"><span data-stu-id="19174-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="19174-229">Dodano opcjonalne parametry do polecenia „Invoke-AzDataFactoryV2Pipeline” w celu obsługi ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="19174-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-231">Dodano opis zmiany powodującej niezgodność dla poleceń „Export-AzDataLakeStoreItem” i „Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="19174-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="19174-232">Dodano opcję kodowania bajtów dla poleceń „New-AzDataLakeStoreItem”, „Add-AzDAtaLakeStoreItemContent” i „Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="19174-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-233">Az.HDInsight</span></span>
* <span data-ttu-id="19174-234">Dodano obsługę określania minimalnej obsługiwanej wersji protokołu TLS podczas tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="19174-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-235">Az.IotHub</span></span>
* <span data-ttu-id="19174-236">Dodano obsługę zarządzania ustawieniami rozproszonymi dla poszczególnych urządzeń.</span><span class="sxs-lookup"><span data-stu-id="19174-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="19174-237">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="19174-238">„Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="19174-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="19174-239">„Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="19174-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-240">Az.KeyVault</span></span>
* <span data-ttu-id="19174-241">Dodano atrybuty zmian powodujących niezgodność do polecenia „New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="19174-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-242">Az.Monitor</span></span>
* <span data-ttu-id="19174-243">Zaktualizowano dokumentację polecenia „New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="19174-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-244">Az.Network</span></span>
* <span data-ttu-id="19174-245">Zaktualizowano polecenia cmdlet, aby zezwolić na połączenia VirtualHubVnetConnections między dzierżawami</span><span class="sxs-lookup"><span data-stu-id="19174-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="19174-246">„New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="19174-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="19174-247">„Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="19174-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="19174-248">„New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="19174-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="19174-249">„Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="19174-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="19174-250">Usunięto zależność od zestawu SDK zarządzania SQL</span><span class="sxs-lookup"><span data-stu-id="19174-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-252">Ulepszono komunikaty o błędach</span><span class="sxs-lookup"><span data-stu-id="19174-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-254">W usłudze Azure Site Recovery dodano obsługę ponownego włączania ochrony oraz zaktualizowano właściwości maszyn wirtualnych w przypadku maszyn wirtualnych zaszyfrowanych za pomocą usługi Azure Disk Encryption.</span><span class="sxs-lookup"><span data-stu-id="19174-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="19174-255">Dodano monitorowanie odzyskiwania po awarii właściwości VmwareToAzure usługi Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="19174-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="19174-256">W usłudze Azure Backup dodano obsługę ponawiania aktualizacji zasad w przypadku elementów, dla których zakończyła się ona niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="19174-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="19174-257">W usłudze Azure Backup dodano obsługę ustawień wykluczania dysków podczas tworzenia i przywracania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="19174-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="19174-258">W usłudze Azure Backup dodano obsługę przywracania wielu plików/folderów w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="19174-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="19174-259">W usłudze Azure Backup dodano obsługę dla określonej przez użytkownika obsługi grupy zasobów w trakcie aktualizowania zasad IaasVM</span><span class="sxs-lookup"><span data-stu-id="19174-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-260">Az.Resources</span></span>
* <span data-ttu-id="19174-261">Poprawiono polecenie „Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType”, aby używało rzeczywistej wersji apiVersion zasobów, a nie domyślnej wersji apiVersion [nr 11267]</span><span class="sxs-lookup"><span data-stu-id="19174-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="19174-262">Dodano rejestrowanie identyfikatorów correlationId dla scenariuszy błędów</span><span class="sxs-lookup"><span data-stu-id="19174-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="19174-263">Niewielka zmiana dokumentacji polecenia „Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="19174-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="19174-264">Dodano przykład.</span><span class="sxs-lookup"><span data-stu-id="19174-264">Added example.</span></span>
* <span data-ttu-id="19174-265">Dodano znak ucieczki przed pojedynczym cudzysłowem w wartości parametru „Get-AzADUser” [nr 11317]</span><span class="sxs-lookup"><span data-stu-id="19174-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="19174-266">Dodano nowe polecenia cmdlet dla skryptów wdrażania („Get-AzDeploymentScript”, „Get-AzDeploymentScriptLog”, „Save-AzDeploymentScriptLog”, „Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="19174-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-267">Az.Sql</span></span>
* <span data-ttu-id="19174-268">Dodano możliwy do odczytu parametr pomocniczy do polecenia „Invoke-AzSqlDatabaseFailover”</span><span class="sxs-lookup"><span data-stu-id="19174-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="19174-269">Dodano polecenie cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication”</span><span class="sxs-lookup"><span data-stu-id="19174-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="19174-270">Zapisywanie stopnia czułości podczas klasyfikowania kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="19174-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="19174-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="19174-271">Az.Support</span></span>
* <span data-ttu-id="19174-272">Ogólna dostępność modułu „Az.Support”</span><span class="sxs-lookup"><span data-stu-id="19174-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-273">Az.Websites</span></span>
* <span data-ttu-id="19174-274">Dodano obsługę pracy z regułami routingu ruchu aplikacji internetowej za pośrednictwem poniższych nowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="19174-275">„Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="19174-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="19174-276">„Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="19174-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="19174-277">„Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="19174-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="19174-278">„Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="19174-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="19174-279">3.6.1 — marzec 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-280">Az.Accounts</span></span>
* <span data-ttu-id="19174-281">Otwarcie strony ankiety Azure PowerShell w poleceniu „Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="19174-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="19174-282">Wyświetlanie adresu URL ankiety Azure PowerShell w poleceniu „Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="19174-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="19174-283">Dodano wersję Az w agencie UserAgent</span><span class="sxs-lookup"><span data-stu-id="19174-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-284">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-285">Dodano obsługę pobierania i konfigurowania domeny niestandardowej w punkcie końcowym DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="19174-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="19174-286">Dodano obsługę elementu „Export-AzApiManagementApi” do pobierania definicji interfejsu API w formacie JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="19174-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="19174-287">Dla polecenia „Import-AzApiManagementApi” dodano obsługę importowania definicji OpenApi 3.0 z dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="19174-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="19174-288">Dla poleceń „New-AzApiManagementIdentityProvider” i „Set-AzApiManagementIdentityProvider” dodano obsługę konfigurowania „dzierżawy podpisującej” dla dostawcy AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="19174-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-290">Dodano odwołanie do elementu System.Buffers jawnie w plikach csproj i psd1.</span><span class="sxs-lookup"><span data-stu-id="19174-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-291">Az.IotHub</span></span>
* <span data-ttu-id="19174-292">Dodano obsługę zarządzania urządzeniami w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="19174-293">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="19174-294">„Add-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-295">„Get-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-296">„Remove-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-297">„Set-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="19174-298">Dodano obsługę zarządzania modułami na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="19174-299">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="19174-300">„Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="19174-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="19174-301">„Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="19174-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="19174-302">„Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="19174-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="19174-303">„Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="19174-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="19174-304">Dodano polecenie cmdlet do pobierania parametrów połączenia docelowego urządzenia IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="19174-305">Dodano polecenie cmdlet do pobierania parametrów połączenia modułu na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="19174-306">Dodano obsługę pobierania/ustawiania urządzenia nadrzędnego urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="19174-307">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="19174-308">„Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="19174-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="19174-309">„Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="19174-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="19174-310">Dodano obsługę zarządzania relacją nadrzędny-podrzędny urządzenia.</span><span class="sxs-lookup"><span data-stu-id="19174-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-311">Az.Monitor</span></span>
* <span data-ttu-id="19174-312">Stała wartość wyjściowa polecenia „Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="19174-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-313">Az.Network</span></span>
* <span data-ttu-id="19174-314">Zaktualizowano zestaw SDK zarządzania SQL.</span><span class="sxs-lookup"><span data-stu-id="19174-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="19174-315">Rozwiązano problem z różnicą nazewnictwa w klasie PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="19174-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="19174-316">Mapowanie pola ActionsRequired na pole ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="19174-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="19174-317">Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="19174-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-318">Az.Resources</span></span>
* <span data-ttu-id="19174-319">Usunięto błąd odwołania o wartości null w elemencie „Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="19174-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="19174-320">Opcje „-Force” i „-PassThru” oznaczono jako opcjonalny w poleceniu „Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="19174-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="19174-321">Rozwiązano problem polegający na tym, że element „MailNickname” nie jest zwracany przez polecenie „Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="19174-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="19174-322">Rozwiązano problem polegający na tym, że operacja potoku „Remove-AzADGroup” nie działa [#11171]</span><span class="sxs-lookup"><span data-stu-id="19174-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="19174-323">Naprawiono błąd odwołania o wartości null w poleceniu GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="19174-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="19174-324">Dodano atrybuty zmiany powodującej niezgodność dla nadchodzących zmian w poleceniach cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="19174-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="19174-325">Zaktualizowano polecenie „Get-AzResourceGroup”, aby można było wykonać filtrowanie tagów grup zasobów po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="19174-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="19174-326">Rozszerzone polecenia cmdlet dotyczące tagów do akceptowania parametru -ResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="19174-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="19174-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="19174-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="19174-330">Dodano nowe polecenie cmdlet dotyczące tagów</span><span class="sxs-lookup"><span data-stu-id="19174-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="19174-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="19174-332">Dodano element ScopedDeployment z zestawu SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="19174-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-333">Az.Sql</span></span>
* <span data-ttu-id="19174-334">Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="19174-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="19174-335">Dodano obsługę konfiguracji długoterminowego przechowywania kopii zapasowych dla zarządzanych baz danych</span><span class="sxs-lookup"><span data-stu-id="19174-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="19174-336">Pobieranie/ustawianie zasad LTR w zarządzanej bazie danych</span><span class="sxs-lookup"><span data-stu-id="19174-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="19174-337">Pobieranie kopii zapasowych LTR według zarządzanej bazy danych, wystąpienia zarządzanego lub lokalizacji</span><span class="sxs-lookup"><span data-stu-id="19174-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="19174-338">Usuwanie kopii zapasowej LTR</span><span class="sxs-lookup"><span data-stu-id="19174-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="19174-339">Przywracanie kopii zapasowej LTR, aby utworzyć nową zarządzaną bazę danych</span><span class="sxs-lookup"><span data-stu-id="19174-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="19174-340">Dodano parametr MinimalTlsVersion do polecenia New-AzSqlServer i Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="19174-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="19174-341">Dodano parametr MinimalTlsVersion do poleceń New-AzSqlInstance i Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="19174-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="19174-342">Niestandardowa wersja zestawu SQL SDK dla elementu Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-343">Az.Storage</span></span>
* <span data-ttu-id="19174-344">Obsługiwane polecenie AllowProtectedAppendWrite w zasadach ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="19174-345">„Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="19174-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="19174-346">Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu AzureStorageTable w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="19174-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="19174-347">„New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="19174-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="19174-348">„Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="19174-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-349">Az.Websites</span></span>
* <span data-ttu-id="19174-350">Dodano parametr tagu dla opcji „New-AzAppServicePlan” i „Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="19174-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="19174-351">Zatrzymaj wykonywanie polecenia cmdlet, jeśli podczas dodawania domeny niestandardowej do witryny internetowej zostanie zgłoszony wyjątek</span><span class="sxs-lookup"><span data-stu-id="19174-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="19174-352">Dodano obsługę wykonywania operacji dla usługi App Services nieznajdujących się w tej samej grupie zasobów co plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="19174-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="19174-353">Zastosowano ograniczenie dostępu do aplikacji internetowych/funkcji w różnych grupach zasobów</span><span class="sxs-lookup"><span data-stu-id="19174-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="19174-354">Rozwiązano problem w celu ustawienia niestandardowych nazw hostów dla miejsc aplikacji internetowych</span><span class="sxs-lookup"><span data-stu-id="19174-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="19174-355">3.5.0 — luty 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-356">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-356">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-357">Zaktualizowano telemetrię po stronie klienta.</span><span class="sxs-lookup"><span data-stu-id="19174-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="19174-358">W module Az.IotHub dodano polecenia cmdlet do obsługi zarządzania urządzeniami.</span><span class="sxs-lookup"><span data-stu-id="19174-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="19174-359">W module Az.SqlVirtualMachine dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="19174-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-360">Az.Accounts</span></span>
* <span data-ttu-id="19174-361">Dodano identyfikatory SubscriptionId i TenantId oraz czas wykonywania do danych telemetrii po stronie klienta</span><span class="sxs-lookup"><span data-stu-id="19174-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-362">Az.Automation</span></span>
* <span data-ttu-id="19174-363">Poprawiono literówkę w 1. przykładzie w dokumentacji referencyjnej polecenia „New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="19174-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-365">Zaktualizowano zestaw SDK do wersji 7.0</span><span class="sxs-lookup"><span data-stu-id="19174-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="19174-366">Ulepszono komunikat o błędzie, gdy odpowiedź serwera ma pustą treść</span><span class="sxs-lookup"><span data-stu-id="19174-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-367">Az.Compute</span></span>
* <span data-ttu-id="19174-368">Dozwolono pustą wartość identyfikatora ProximityPlacementGroupId podczas aktualizacji</span><span class="sxs-lookup"><span data-stu-id="19174-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-369">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-370">Dodano polecenie cmdlet służące do pobierania definicji reguł zarządzanych, które mogą być używane w zaporze aplikacji internetowej</span><span class="sxs-lookup"><span data-stu-id="19174-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-371">Az.IotHub</span></span>
* <span data-ttu-id="19174-372">Dodano obsługę zarządzania urządzeniami w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="19174-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="19174-373">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="19174-374">„Add-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-375">„Get-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-376">„Remove-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="19174-377">„Set-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="19174-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-378">Az.KeyVault</span></span>
* <span data-ttu-id="19174-379">Poprawiono zduplikowany tekst pliku Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="19174-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-380">Az.Monitor</span></span>
* <span data-ttu-id="19174-381">Poprawiono opis polecenia cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="19174-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="19174-382">Do polecenia „New-AzMetricAlertRuleV2” dodano nowy parametr o nazwie ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="19174-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="19174-383">Użytkownik może podać wartość ActionGroupId(ciąg) lub ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="19174-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-384">Az.Network</span></span>
* <span data-ttu-id="19174-385">Dodano jedną dodatkową uwagę dla parametru „-EnableProxyProtocol” polecenia cmdlet „New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="19174-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="19174-386">Poprawiono przykład opcji FilterData w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="19174-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="19174-387">Dodano przykład przechwytywania pakietów przedstawiający przechwytywanie wszystkich pakietów wewnętrznych i zewnętrznych w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="19174-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="19174-388">Obsługa zasad usługi Azure Firewall w przypadku zapór sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="19174-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="19174-389">Nie dodano żadnych nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-389">No new cmdlets are added.</span></span> <span data-ttu-id="19174-390">Złagodzono ograniczenie dotyczące zasad zapór sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="19174-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-392">Dodano obsługę funkcji przywracania jako plików dla baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="19174-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-393">Az.Resources</span></span>
* <span data-ttu-id="19174-394">Refaktoryzowano polecenia cmdlet wdrażania szablonów</span><span class="sxs-lookup"><span data-stu-id="19174-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="19174-395">Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w grupie zarządzania: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="19174-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="19174-396">Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w zakresie dzierżawy: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="19174-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="19174-397">Refaktoryzowano polecenia cmdlet \*-AzDeployment tak, aby działały konkretnie w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="19174-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="19174-398">Utworzono aliasy \*-AzSubscriptionDeployment dla poleceń cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="19174-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="19174-399">Poprawiono polecenie „Update-AzADApplication”, gdy parametr „AvailableToOtherTenants” nie jest ustawiony</span><span class="sxs-lookup"><span data-stu-id="19174-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="19174-400">Usunięto zestaw parametrów ApplicationObjectWithoutCredentialParameterSet, aby uniknąć wyjątku AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="19174-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="19174-401">Ponownie wygenerowano pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-402">Az.Sql</span></span>
* <span data-ttu-id="19174-403">Dodano obsługę przywracania do punktu w czasie w wystąpieniach zarządzanych między subskrypcjami.</span><span class="sxs-lookup"><span data-stu-id="19174-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="19174-404">Dodano obsługę zmiany obecnej generacji sprzętu wystąpienia zarządzanego SQL</span><span class="sxs-lookup"><span data-stu-id="19174-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="19174-405">Poprawiono przykłady w pomocy polecenia „Update-AzSqlServerVulnerabilityAssessmentSetting”: dane wyjściowe parametru/właściwości — EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="19174-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="19174-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="19174-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="19174-407">Dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="19174-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="19174-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="19174-408">Az.StorageSync</span></span>
* <span data-ttu-id="19174-409">Zaktualizowano obsługiwane zestawy znaków w poleceniu „Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="19174-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="19174-410">3.4.0 — luty 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-411">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-411">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-412">Wydano początkową wersję 0.1.0 funkcji Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="19174-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="19174-413">Dodano obsługę funkcji Az.Network ConnectionMonitor w wersji 2</span><span class="sxs-lookup"><span data-stu-id="19174-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-414">Az.Accounts</span></span>
* <span data-ttu-id="19174-415">Wyłączono automatyczne zapisywanie kontekstu, gdy plik AzureRmContext.json jest niedostępny</span><span class="sxs-lookup"><span data-stu-id="19174-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="19174-416">Zaktualizowano odwołania do programu Azure PowerShell Common do wersji 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="19174-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-417">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-418">**Get-AzApiManagementApiSchema** Naprawiono pobieranie schematu Open-Api skojarzonego z interfejsem API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="19174-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="19174-419">**New-AzApiManagementProduct**\* i **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="19174-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="19174-420">Poprawiono dokumentację dotycząca funkcji https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="19174-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="19174-421">**Set-AzApiManagementApi** Dodano przykład pokazujący, jak zaktualizować wartość ServiceUrl przy użyciu polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-422">Az.Compute</span></span>
* <span data-ttu-id="19174-423">Ograniczono liczbę stanów maszyn wirtualnych do 100, aby uniknąć ograniczania w przypadku wykonywania operacji Get-AzVM -Status bez nazwy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="19174-424">Dodano polecenie cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="19174-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="19174-425">Dodano parametry EncryptionType i DiskEncryptionSetId do następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="19174-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="19174-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="19174-427">Dodano parametr ColocationStatus do polecenia cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="19174-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-428">Az.DataFactory</span></span>
* <span data-ttu-id="19174-429">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.7.0</span><span class="sxs-lookup"><span data-stu-id="19174-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="19174-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="19174-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="19174-431">Dodano operacje LIST dla zasobów</span><span class="sxs-lookup"><span data-stu-id="19174-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="19174-432">Dodano możliwość wykonywania operacji na krokach kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="19174-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-433">Az.HDInsight</span></span>
* <span data-ttu-id="19174-434">Naprawiono błąd w dokumentacji funkcji New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="19174-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-435">Az.KeyVault</span></span>
* <span data-ttu-id="19174-436">Dodano alias Name do atrybutu VaultName, aby uspójnić polecenie Remove-AzureKeyVault z poleceniem New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="19174-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-437">Az.Network</span></span>
* <span data-ttu-id="19174-438">Dodano nowy przykład do polecenia Set-AzNetworkWatcherConfigFlowLog.md w celu zademonstrowania scenariusza wyłączenia analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="19174-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="19174-439">Dodano obsługę przypisywania konfiguracji protokołu IP zarządzania do zapory Azure Firewall — dedykowanej podsieci i publicznego adresu IP, których zapora będzie używać dla swojego ruchu związanego z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="19174-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="19174-440">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="19174-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="19174-441">Dodano parametr -ManagementPublicIpAddress (nieobowiązkowy), który akceptuje obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="19174-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="19174-442">Dodano metodę SetManagementIpConfiguration w obiekcie zapory — wymaga jako danych wejściowych podsieci i publicznego adresu IP — nazwa podsieci musi mieć wartość „AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="19174-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="19174-443">Poprawiono przykłady polecenia Get-AzNetworkSecurityGroup, aby pokazać przykłady dla sieciowej grupy zabezpieczeń zamiast interfejsów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19174-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="19174-444">Poprawiono literówkę w poleceniu New-AzVpnSite, która uniemożliwiała modułowi wypełniania identyfikatora wypełnienie parametru.</span><span class="sxs-lookup"><span data-stu-id="19174-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="19174-445">Dodano obsługę konfiguracji adresu URL w akcji reguł ponownego zapisywania ustawionej w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="19174-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="19174-446">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-446">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="19174-448">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="19174-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="19174-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="19174-450">Dodano obsługę dla zasobów NetworkWatcher ConnectionMonitor w wersji 2</span><span class="sxs-lookup"><span data-stu-id="19174-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-452">Obsługa oceny zgodności przed ustaleniem, który zasób należy skorygować</span><span class="sxs-lookup"><span data-stu-id="19174-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="19174-453">Dodano parametr „-ResourceDiscoverMode” do polecenia Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="19174-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="19174-454">Dodano polecenie cmdlet Get-AzPolicyMetadata na potrzeby pobierania zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="19174-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="19174-455">Zaktualizowano polecenia Get-AzPolicyState i Get-AzPolicyStateSummary dla interfejsu API w wersji 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="19174-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-457">Usługa Azure Site Recovery obsługuje usuwanie zreplikowanego dysku.</span><span class="sxs-lookup"><span data-stu-id="19174-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="19174-458">W usłudze Azure Backup dodano obsługę dodawania tagów podczas tworzenia magazynu usługi Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="19174-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-459">Az.Resources</span></span>
* <span data-ttu-id="19174-460">Parametr -Scope ustawiono jako opcjonalny w poleceniach cmdlet \*-AzPolicyAssignment z domyślną wartością subskrypcji kontekstu</span><span class="sxs-lookup"><span data-stu-id="19174-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="19174-461">Dodano przykłady tworzenia obiektu ADServicePrincipal z hasłem i kluczowym poświadczeniem</span><span class="sxs-lookup"><span data-stu-id="19174-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-462">Az.Sql</span></span>
<span data-ttu-id="19174-463">Naprawiono polecenie cmdlet New-AzSqlDatabaseSecondary, aby sprawdzało istnienie elementu PartnerDatabaseName zamiast istnienia elementu DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="19174-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-464">Az.Storage</span></span>
* <span data-ttu-id="19174-465">Włączono obsługę typu klucza szyfrowania tabeli/kolejki w tworzeniu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="19174-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="19174-467">Pokazywana jest wartość RequestId, gdy właściwość StorageException nie ma wartości ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="19174-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="19174-468">Poprawiono przykład 6 polecenia cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="19174-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-469">Az.Websites</span></span>
* <span data-ttu-id="19174-470">Polecenia Set-AzWebapp i Set-AzWebappSlot obsługują właściwości AlwaysOn, MinTls i FtpsState</span><span class="sxs-lookup"><span data-stu-id="19174-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="19174-471">Rozwiązywanie problemu polegającego na tym, że zmienianie ustawienia HttpsOnly jednocześnie ze zmienianiem ustawienia AppservicePlan za pomocą jednego polecenia Set-AzWebApp powodowało resetowanie ustawienia HttpsOnly do wartości domyślnej</span><span class="sxs-lookup"><span data-stu-id="19174-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="19174-472">3.3.0 — styczeń 2020 r.</span><span class="sxs-lookup"><span data-stu-id="19174-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-473">Az.Accounts</span></span>
* <span data-ttu-id="19174-474">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametry AzureAttestationServiceEndpointResourceId i AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="19174-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-475">Az.Cdn</span></span>
* <span data-ttu-id="19174-476">Wyświetlanie szczegółów odpowiedzi błędu w poleceniu cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-477">Az.Compute</span></span>
* <span data-ttu-id="19174-478">Poprawiono polecenie cmdlet Set-AzVMCustomScriptExtension dla maszyny wirtualnej z zarządzanym dyskiem systemu operacyjnego, który nie ma profilu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="19174-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="19174-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="19174-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="19174-480">Naprawiono nazwy parametrów używanych na przykład przez polecenie New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="19174-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="19174-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="19174-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="19174-482">Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="19174-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="19174-483">Pobieranie kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="19174-484">Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="19174-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="19174-485">Tworzenie nowego kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="19174-486">Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="19174-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="19174-487">Usuwanie kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="19174-488">Dodano polecenie cmdlet „Invoke-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="19174-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="19174-489">Wywoływanie akcji odświeżania danych w kontenerze magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="19174-490">Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="19174-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="19174-491">Pobieranie konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="19174-492">Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="19174-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="19174-493">Tworzenie nowego konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="19174-494">Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="19174-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="19174-495">Usuwanie konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="19174-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="19174-496">Wywołanie polecenia cmdlet „Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="19174-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="19174-497">Wywołanie akcji odświeżania danych w udziale</span><span class="sxs-lookup"><span data-stu-id="19174-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="19174-498">Dodano polecenie cmdlet „Set-AzDataBoxEdgeStorageAccountCredential”</span><span class="sxs-lookup"><span data-stu-id="19174-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="19174-499">Ustawienie poświadczenia konta magazynu az databoxedge</span><span class="sxs-lookup"><span data-stu-id="19174-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-500">Az.DataFactory</span></span>
* <span data-ttu-id="19174-501">Dodano właściwości AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId i VersionStatus do polecenia Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="19174-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="19174-502">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.6.0</span><span class="sxs-lookup"><span data-stu-id="19174-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="19174-503">Dodano parametr „PublicIPs” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu umożliwienia tworzenia środowisk IR Azure-SSIS ze statycznymi publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="19174-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="19174-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="19174-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="19174-505">Usunięto niedziałający link w pliku Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="19174-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-506">Az.EventHub</span></span>
* <span data-ttu-id="19174-507">Rozwiązano problem nr 10634: Naprawiono odwołanie do obiektu null podczas usuwania elementu eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="19174-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-508">Az.HDInsight</span></span>
* <span data-ttu-id="19174-509">Poprawiono błąd w pliku Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="19174-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="19174-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="19174-510">Az.MachineLearning</span></span>
* <span data-ttu-id="19174-511">Usunięto poniższe polecenia cmdlet, ponieważ funkcja MachineLearningCompute nie jest już dostępna</span><span class="sxs-lookup"><span data-stu-id="19174-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="19174-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="19174-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="19174-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="19174-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="19174-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="19174-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="19174-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="19174-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="19174-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="19174-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="19174-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="19174-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="19174-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="19174-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-519">Az.Network</span></span>
* <span data-ttu-id="19174-520">Uaktualniono zależność Microsoft.Azure.Management.Sql z wersji 1.36-preview do 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="19174-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-522">W usłudze Azure Site Recovery zmieniono obsługę maszyn wirtualnych z dyskiem zarządzanym szyfrowanych podczas magazynowania za pomocą kluczy zarządzanych przez klienta dla platformy Azure na dostawcę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="19174-523">Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego podczas włączania ochrony dla narzędzia VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="19174-524">Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego na poziomie dysku w celu włączenia ochrony dla narzędzia VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="19174-525">Usługa Azure Site Recovery obsługuje aktualizację elementu chronionego przez replikację z zestawem szyfrowania dysków mapowanym dla funkcji HyperV na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-526">Az.Resources</span></span>
* <span data-ttu-id="19174-527">Naprawiono błąd w dokumencie pomocy „Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="19174-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-528">Az.Sql</span></span>
* <span data-ttu-id="19174-529">Naprawiono błąd oceny luk w zabezpieczeniach dotyczący funkcji poleceń cmdlet do ustawiania punktu odniesienia w celu działania na bazie danych master dla usługi Azure Database i ograniczenia go w systemowych bazach danych wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19174-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="19174-530">Naprawiono błąd podczas tworzenia grupy trybu failover wystąpienia SQL</span><span class="sxs-lookup"><span data-stu-id="19174-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="19174-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="19174-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="19174-532">Dodano nowy prawidłowy typ licencji DR</span><span class="sxs-lookup"><span data-stu-id="19174-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-533">Az.Storage</span></span>
* <span data-ttu-id="19174-534">Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu DefaultAction w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="19174-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="19174-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="19174-536">Obsługa uzyskiwania ostatniego czasu synchronizacji kont usługi Storage poprzez uruchomienie polecenia get-AzureRMStorageAccount z parametrem -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="19174-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="19174-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="19174-538">3.2.0 — grudzień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="19174-539">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-539">General</span></span>
* <span data-ttu-id="19174-540">Zaktualizowano odwołania w pliku psd1 tak, aby dla wszystkich modułów były używane ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="19174-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-541">Az.Accounts</span></span>
* <span data-ttu-id="19174-542">Ustawiono prawidłowego agenta użytkownika dla telemetrii po stronie klienta dla modułu Az 4.0 (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="19174-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="19174-543">Wyświetlanie przyjaznego dla użytkownika komunikatu o błędzie, gdy kontekst ma wartość null, w module Az 4.0 (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="19174-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="19174-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-544">Az.Batch</span></span>
* <span data-ttu-id="19174-545">Rozwiązano problem [nr 10602](https://github.com/Azure/azure-powershell/issues/10602) uniemożliwiający poleceniu **New-AzBatchPool** prawidłowe wysyłanie elementów „VirtualMachineConfiguration.ContainerConfiguration” i „VirtualMachineConfiguration.DataDisks” do serwera.</span><span class="sxs-lookup"><span data-stu-id="19174-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-546">Az.DataFactory</span></span>
* <span data-ttu-id="19174-547">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.5.0</span><span class="sxs-lookup"><span data-stu-id="19174-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-548">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-549">Dodano obsługę wykluczania reguł zarządzanych przez zaporę aplikacji internetowej</span><span class="sxs-lookup"><span data-stu-id="19174-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="19174-550">Dodano element SocketAddr do autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="19174-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="19174-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="19174-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="19174-552">Obsługa wyjątków</span><span class="sxs-lookup"><span data-stu-id="19174-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-553">Az.KeyVault</span></span>
* <span data-ttu-id="19174-554">Usunięto błąd podczas uzyskiwania dostępu do wartości, która potencjalnie nie jest ustawiona</span><span class="sxs-lookup"><span data-stu-id="19174-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="19174-555">Zarządzanie certyfikatami kryptografii opartej na krzywej eliptycznej</span><span class="sxs-lookup"><span data-stu-id="19174-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="19174-556">Dodano obsługę określania krzywej dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="19174-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-557">Az.Monitor</span></span>
* <span data-ttu-id="19174-558">Dodanie opcjonalnego argumentu do polecenia dodania ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="19174-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="19174-559">Argument przełącznika, który, jeśli zostanie podany, wskazuje, że eksportowanie do usługi Log Analytics musi być przeprowadzane do ustalonego schematu (tzn.</span><span class="sxs-lookup"><span data-stu-id="19174-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="19174-560">typu danych, dedykowanego)</span><span class="sxs-lookup"><span data-stu-id="19174-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-561">Az.Network</span></span>
* <span data-ttu-id="19174-562">Obsługa grup adresów IP w regułach sieci, translatorze adresów sieciowych i aplikacji usługi Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="19174-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-563">Az.Resources</span></span>
* <span data-ttu-id="19174-564">Usunięto problem polegający na tym, że wdrożenie szablonu nie może odczytać parametru szablonu, jeśli jego nazwa powoduje konflikt z nazwą wbudowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="19174-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="19174-565">Zaktualizowano polecenia cmdlet zasad w celu używania nowej wersji interfejsu API 2019-09-01, która wprowadza obsługę grupowania w definicjach zestawów zasad.</span><span class="sxs-lookup"><span data-stu-id="19174-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-566">Az.Sql</span></span>
* <span data-ttu-id="19174-567">Uaktualniono tworzenie magazynu w automatycznym włączaniu oceny luk w zabezpieczeniach do wersji StorageV2</span><span class="sxs-lookup"><span data-stu-id="19174-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-568">Az.Storage</span></span>
* <span data-ttu-id="19174-569">Obsługa generowania tokenów SAS opartych na tożsamości kontenera / obiektu blob z kontekstem magazynu w oparciu o uwierzytelnianie OAuth</span><span class="sxs-lookup"><span data-stu-id="19174-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="19174-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="19174-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="19174-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="19174-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="19174-572">Obsługa odwoływania kluczy delegowania użytkowników dla konta magazynu w celu odwołania wszystkich tokenów SAS tożsamości</span><span class="sxs-lookup"><span data-stu-id="19174-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="19174-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="19174-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="19174-574">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 14.2.0 w celu obsługi nowego interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="19174-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="19174-575">Obsługa funkcji QuotaGiB (udostępnianie limitu przydziału w GiB) dla wartości powyżej 5120 w poleceniach cmdlet płaszczyzny zarządzania udziałem plików i dodano alias parametru „Quota” do parametru „QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="19174-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="19174-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="19174-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="19174-578">Dodano alias parametru „QuotaGiB” do parametru „Quota”</span><span class="sxs-lookup"><span data-stu-id="19174-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="19174-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="19174-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="19174-580">Rozwiązano problem z czyszczeniem zapisanych zasad dostępu przez polecenie Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="19174-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="19174-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="19174-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="19174-582">3.1.0 — listopad 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-583">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-583">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-584">Wydano pakiet Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="19174-585">Wydano pakiet Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-586">Az.Compute</span></span>
* <span data-ttu-id="19174-587">Funkcja ponownego stosowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-587">VM Reapply feature</span></span>
    - <span data-ttu-id="19174-588">Dodano parametr Reapply do polecenia cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="19174-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="19174-589">Funkcja AutomaticRepairs zestawu skalowania maszyn wirtualnych:</span><span class="sxs-lookup"><span data-stu-id="19174-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="19174-590">Dodano parametry EnableAutomaticRepair, AutomaticRepairGracePeriod i AutomaticRepairMaxInstanceRepairsPercent do następujących poleceń cmdlet:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="19174-591">Obsługa obrazów z galerii pomiędzy dzierżawami dla polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="19174-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="19174-592">Dodano element „Spot” do modułu wypełniania argumentów parametru Priority w poleceniach cmdlet New-AzVM, New-AzVMConfig i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="19174-593">Dodano parametry DiskIOPSReadWrite i DiskMBpsReadWrite do polecenia cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="19174-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="19174-594">Zmieniono parametr SourceImageId polecenia cmdlet New-AzGalleryImageVersion na opcjonalny</span><span class="sxs-lookup"><span data-stu-id="19174-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="19174-595">Dodano parametry OSDiskImage i DataDiskImage do polecenia cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="19174-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="19174-596">Dodano parametr HyperVGeneration do polecenia cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="19174-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="19174-597">Dodano parametry SkipExtensionsOnOverprovisionedVMs do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="19174-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="19174-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="19174-599">Dodano polecenie cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="19174-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="19174-600">Pobieranie zamówienia</span><span class="sxs-lookup"><span data-stu-id="19174-600">Get the Order</span></span>
* <span data-ttu-id="19174-601">Dodano polecenie cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="19174-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="19174-602">Utworzono nowe zamówienie</span><span class="sxs-lookup"><span data-stu-id="19174-602">Create new Order</span></span>
* <span data-ttu-id="19174-603">Dodano polecenie cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="19174-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="19174-604">Usunięto zamówienie</span><span class="sxs-lookup"><span data-stu-id="19174-604">Remove the Order</span></span>
* <span data-ttu-id="19174-605">Zmiana w poleceniu cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="19174-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="19174-606">Teraz tworzy lokalny udział plików</span><span class="sxs-lookup"><span data-stu-id="19174-606">Now creates Local Share</span></span>
* <span data-ttu-id="19174-607">Dodano polecenie cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="19174-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="19174-608">Teraz można zamapować wartość IotRole na udział plików</span><span class="sxs-lookup"><span data-stu-id="19174-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="19174-609">Dodano polecenie cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="19174-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="19174-610">Wywoływanie skanowania aktualizacji, pobierania aktualizacji, instalowania aktualizacji na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="19174-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="19174-611">Dodano polecenie cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="19174-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="19174-612">Pobiera informacje o wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="19174-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="19174-613">Dodano polecenie cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="19174-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="19174-614">Utworzono nowe wyzwalacze</span><span class="sxs-lookup"><span data-stu-id="19174-614">Create new Triggers</span></span>
* <span data-ttu-id="19174-615">Dodano polecenie cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="19174-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="19174-616">Usunięto wyzwalacze</span><span class="sxs-lookup"><span data-stu-id="19174-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-617">Az.DataFactory</span></span>
* <span data-ttu-id="19174-618">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.4.0</span><span class="sxs-lookup"><span data-stu-id="19174-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="19174-619">Dodano parametr „ExpressCustomSetup” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu włączenia konfiguracji i składników innych firm bez niestandardowego skryptu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="19174-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-621">Zaktualizowano dokumentację poleceń Get-AzDataLakeStoreDeletedItem i Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="19174-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-622">Az.EventHub</span></span>
* <span data-ttu-id="19174-623">Rozwiązano problem nr 10301: Poprawiono format daty tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="19174-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-624">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-625">Dodano parametr MinimumTlsVersion do poleceń Enable-AzFrontDoorCustomDomainHttps i New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="19174-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="19174-626">Dodano parametry HealthProbeMethod i EnabledState do polecenia New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="19174-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="19174-627">Dodano nowe polecenie cmdlet do tworzenia obiektu BackendPoolsSettings w celu przejścia do tworzenia/aktualizacji usługi Front Door</span><span class="sxs-lookup"><span data-stu-id="19174-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="19174-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="19174-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-629">Az.Network</span></span>
* <span data-ttu-id="19174-630">Zmieniono przykłady opcji FilterData dla plików „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md” i „Start-AzVirtualnetworkGatewayPacketCapture.md”.</span><span class="sxs-lookup"><span data-stu-id="19174-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="19174-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="19174-631">Az.PrivateDns</span></span>
* <span data-ttu-id="19174-632">Zaktualizowano zestaw .Net SDK usługi PrivateDns do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-634">Obsługa usługi Azure Site Recovery w celu wybrania typu dysku przy włączaniu ochrony.</span><span class="sxs-lookup"><span data-stu-id="19174-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="19174-635">Poprawka edycji akcji planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="19174-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="19174-636">Obsługa przywracania SQL usługi Azure Backup w celu akceptowania baz danych strumienia pliku.</span><span class="sxs-lookup"><span data-stu-id="19174-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="19174-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="19174-637">Az.RedisCache</span></span>
* <span data-ttu-id="19174-638">Dodano parametr „MinimumTlsVersion” w poleceniach cmdlet „New-AzRedisCache” i „Set-AzRedisCache”.</span><span class="sxs-lookup"><span data-stu-id="19174-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="19174-639">Ponadto dodano parametr „MinimumTlsVersion” do danych wyjściowych polecenia cmdlet „Get-AzRedisCache”.</span><span class="sxs-lookup"><span data-stu-id="19174-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="19174-640">Dodano weryfikację parametru „-Size” dla poleceń cmdlet „Set-AzRedisCache” i „New-AzRedisCache”</span><span class="sxs-lookup"><span data-stu-id="19174-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-641">Az.Resources</span></span>
- <span data-ttu-id="19174-642">Zaktualizowano polecenia cmdlet zasad, aby używały nowego interfejsu API w wersji 2019-06-01, który ma nową właściwość EnforcementMode w przypisaniu zasad.</span><span class="sxs-lookup"><span data-stu-id="19174-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="19174-643">Zaktualizowano przykład pomocy definicji zasad tworzenia</span><span class="sxs-lookup"><span data-stu-id="19174-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="19174-644">Usunięto usterkę polegającą na tym, że polecenie Remove-AZADServicePrincipal -ServicePrincipalName zwracało pustą referencję, gdy nie znajdowano głównej nazwy usługi.</span><span class="sxs-lookup"><span data-stu-id="19174-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="19174-645">Usunięto usterkę polegającą na tym, że polecenie New-AZADServicePrincipal zwracało pustą referencję, gdy dzierżawa nie miała żadnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="19174-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="19174-646">Zmieniono polecenie New-AzAdServicePrincipal w celu dodania poświadczeń tylko do skojarzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="19174-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-647">Az.Sql</span></span>
* <span data-ttu-id="19174-648">Dodano obsługę bazy danych ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="19174-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="19174-649">Naprawiono polecenie Set-AzSqlDatabase w przypadku, gdy nie ustawiono nadmiarowości strefy</span><span class="sxs-lookup"><span data-stu-id="19174-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="19174-650">3.0.0 — listopad 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="19174-651">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-651">General</span></span>
* <span data-ttu-id="19174-652">Wydano pakiet Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-653">Az.Accounts</span></span>
* <span data-ttu-id="19174-654">Dodano komunikat o zakończeniu obsługi aliasu „Resolve-Error”.</span><span class="sxs-lookup"><span data-stu-id="19174-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="19174-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="19174-655">Az.Advisor</span></span>
* <span data-ttu-id="19174-656">Dodano nową kategorię „Operational Excellence” do polecenia cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="19174-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="19174-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-657">Az.Batch</span></span>
* <span data-ttu-id="19174-658">Nazwę elementu `CoreQuota` dla klasy `BatchAccountContext` zmieniono na `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="19174-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="19174-659">Jest również nowa właściwość `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="19174-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="19174-660">Ma to wpływ na polecenie **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="19174-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="19174-661">Parametr polecenia cmdlet **New-AzBatchTask** `-ResourceFile` teraz przyjmuje kolekcję obiektów `PSResourceFile`, którą można utworzyć przy użyciu nowego polecenia cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="19174-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="19174-662">Nowe polecenie cmdlet **New-AzBatchResourceFile** w celu ułatwienia tworzenia obiektów `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="19174-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="19174-663">Można je dostarczyć do polecenia cmdlet **New-AzBatchTask** w parametrze `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="19174-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="19174-664">Obsługuje ono dwa nowe rodzaje plików zasobów oprócz istniejącego sposobu `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="19174-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="19174-665">Pliki zasobów oparte na elemencie `AutoStorageContainerName` pobierają cały kontener automatycznego magazynu do węzła usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="19174-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="19174-666">Pliki zasobów oparte na elemencie `StorageContainerUrl` pobierają kontener określony w adresie URL do węzła usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="19174-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="19174-667">Usunięto właściwość `ApplicationPackages` elementu `PSApplication` zwracaną przez polecenie cmdlet **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="19174-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="19174-668">Określone pakiety wewnątrz aplikacji można teraz pobrać przy użyciu polecenia cmdlet **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="19174-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="19174-669">Na przykład: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="19174-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="19174-670">Zmieniono nazwę właściwości `ApplicationId` na `ApplicationName` w poleceniach cmdlet **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** i **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="19174-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="19174-671">`ApplicationId` teraz jest aliasem `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="19174-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="19174-672">Dodano nową właściwość `PSWindowsUserConfiguration` do klasy `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="19174-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="19174-673">Zmieniono nazwę właściwości `Version` na `Name` w klasie `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="19174-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="19174-674">Zmieniono nazwę właściwości `BlobSource` na `HttpUrl` w klasie `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="19174-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="19174-675">Usunięto właściwość `OSDisk` z klasy `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="19174-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="19174-676">Usunięto polecenie cmdlet **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="19174-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="19174-677">Ta operacja nie jest już obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="19174-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="19174-678">Usunięto właściwość `TargetOSVersion` z klasy `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="19174-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="19174-679">Zmieniono nazwę właściwości `CurrentOSVersion` na `OSVersion` w klasie `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="19174-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="19174-680">Usunięto właściwości `DataEgressGiB` i `DataIngressGiB` z klasy `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="19174-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="19174-681">Usunięto polecenie cmdlet **Get-AzBatchNodeAgentSku** i zastąpiono je poleceniem cmdlet **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="19174-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="19174-682">Polecenie cmdlet **Get-AzBatchSupportedImage** zwraca te same dane co polecenie cmdlet **Get-AzBatchNodeAgentSku**, ale w bardziej przyjaznym formacie.</span><span class="sxs-lookup"><span data-stu-id="19174-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="19174-683">Teraz są również zwracane nowe obrazy niezweryfikowane.</span><span class="sxs-lookup"><span data-stu-id="19174-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="19174-684">Uwzględniono również dodatkowe informacje na temat właściwości `Capabilities` i `BatchSupportEndOfLife` dla każdego obrazu.</span><span class="sxs-lookup"><span data-stu-id="19174-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="19174-685">Dodano możliwość instalowania zdalnych systemów plików na każdym węźle puli za pośrednictwem nowego parametru `MountConfiguration` polecenia cmdlet **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="19174-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="19174-686">Teraz obsługiwane są reguły zabezpieczeń sieciowych blokujące dostęp sieciowy do puli na podstawie portu źródłowego ruchu.</span><span class="sxs-lookup"><span data-stu-id="19174-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="19174-687">Jest to realizowane za pomocą właściwości `SourcePortRanges` w klasie `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="19174-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="19174-688">Podczas uruchamiania kontenera usługa Batch obsługuje teraz wykonywanie zadania w katalogu roboczym kontenera lub w katalogu roboczym zadania usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="19174-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="19174-689">Jest to kontrolowane przez właściwość `WorkingDirectory` w klasie `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="19174-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="19174-690">Dodano możliwość określania kolekcji publicznych adresów IP w klasie `PSNetworkConfiguration` za pośrednictwem nowej właściwości `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="19174-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="19174-691">To gwarantuje, że węzły w puli będą miały adres IP z listy adresów IP dostarczonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="19174-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="19174-692">Gdy nie zostanie określona, wartością domyślną opcji `WaitForSuccess` w klasie `PSSTartTask` jest teraz `$True` (była wartość `$False`).</span><span class="sxs-lookup"><span data-stu-id="19174-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="19174-693">Gdy nie zostanie określona, wartością domyślną opcji `Scope` w klasie `PSAutoUserSpecification` jest teraz `Pool` (była wartość `Task` w systemie Windows i `Pool` w systemie Linux).</span><span class="sxs-lookup"><span data-stu-id="19174-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-694">Az.Cdn</span></span>
* <span data-ttu-id="19174-695">Wprowadzono akcje UrlRewriteAction i CacheKeyQueryStringAction do aparatu RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="19174-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="19174-696">Usunięto kilka usterek, takich jak brakujące dane wejściowe „Selector” w poleceniu cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="19174-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-697">Az.Compute</span></span>
* <span data-ttu-id="19174-698">Funkcja zestawu szyfrowania dysków</span><span class="sxs-lookup"><span data-stu-id="19174-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="19174-699">Nowe polecenia cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="19174-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="19174-700">Dodano parametr DiskEncryptionSetId do następujących poleceń cmdlet:   Set-AzImageOSDisk, Set-AzVMOSDisk, Set-AzVmssStorageProfile, Add-AzImageDataDisk, New-AzVMDataDisk, Set-AzVMDataDisk, Add-AzVMDataDisk, Add-AzVmssDataDisk i Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="19174-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="19174-701">Dodano parametry DiskEncryptionSetId i EncryptionType do następujących poleceń cmdlet:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="19174-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="19174-702">Dodano parametr Add PublicIPAddressVersion do polecenia cmdlet New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="19174-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="19174-703">Właściwość FileUris rozszerzenia niestandardowego skryptu przeniesiono z ustawienia publicznego do ustawienia chronionego</span><span class="sxs-lookup"><span data-stu-id="19174-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="19174-704">Dodano parametr ScaleInPolicy do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="19174-705">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="19174-705">Breaking changes</span></span>
    - <span data-ttu-id="19174-706">Parametr UploadSizeInBytes jest używany zamiast parametru DiskSizeGB dla polecenia cmdlet New-AzDiskConfig, gdy opcja CreateOption ma wartość Upload</span><span class="sxs-lookup"><span data-stu-id="19174-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="19174-707">Element PublishingProfile.Source.ManagedImage.Id został zastąpiony elementem StorageProfile.Source.Id w obiekcie GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="19174-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-708">Az.DataFactory</span></span>
* <span data-ttu-id="19174-709">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.3.0</span><span class="sxs-lookup"><span data-stu-id="19174-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-711">Aktualizacja wersji zestawu SDK ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), wprowadza następujące poprawki</span><span class="sxs-lookup"><span data-stu-id="19174-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="19174-712">Unikanie zgłaszania wyjątku, gdy nie można zdeserializować elementu creationtime wpisu kosza lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="19174-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="19174-713">Uwidacznianie ustawienia dla limitu czasu żądania w obiekcie adlsclient</span><span class="sxs-lookup"><span data-stu-id="19174-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="19174-714">Naprawiono przekazywanie oryginalnej flagi syncflag na potrzeby odzyskiwania badoffset</span><span class="sxs-lookup"><span data-stu-id="19174-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="19174-715">Naprawiono klasę EnumerateDirectory, aby pobierała token kontynuacji po sprawdzeniu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="19174-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="19174-716">Usunięto usterkę metody Concat</span><span class="sxs-lookup"><span data-stu-id="19174-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-717">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-718">Poprawiono różne literówki w module</span><span class="sxs-lookup"><span data-stu-id="19174-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-719">Az.HDInsight</span></span>
* <span data-ttu-id="19174-720">Usunięto usterkę polegającą na tym, że klient otrzymywał błąd „Nieprawidłowy ciąg Base-64” podczas używania polecenia cmdlet Get-AzHDInsightCluster do pobrania klastra za pomocą magazynu usługi ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="19174-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="19174-721">Dodano parametr o nazwie „ApplicationId” do trzech poleceń cmdlet: Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig i New-AzHDInsightCluster, aby klient mógł podać identyfikator aplikacji jednostki usługi na potrzeby uzyskiwania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="19174-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="19174-722">Zmieniono ustawienie Microsoft.Azure.Management.HDInsight z 2.1.0 na 5.1.0</span><span class="sxs-lookup"><span data-stu-id="19174-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="19174-723">Usunięto pięć poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="19174-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="19174-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="19174-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="19174-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="19174-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="19174-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="19174-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19174-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="19174-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19174-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="19174-729">Dodano trzy polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="19174-730">Get-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="19174-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="19174-731">Enable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="19174-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="19174-732">Disable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="19174-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="19174-733">Naprawiono polecenie cmdlet Get-AzHDInsightProperties w celu obsługi pobierania informacji o możliwościach z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="19174-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="19174-734">Usunięto zestawy parametrów („Spark1”, „Spark2”) z polecenia cmdlet Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="19174-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="19174-735">Dodano przykłady do dokumentów pomocy polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="19174-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="19174-736">Zmieniono typ danych wyjściowych następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="19174-737">Typ danych wyjściowych polecenia cmdlet Get-AzHDInsightProperties zmieniono z CapabilitiesResponse na AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="19174-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="19174-738">Typ danych wyjściowych polecenia cmdlet Remove-AzHDInsightCluster zmieniono z ClusterGetResponse na bool.</span><span class="sxs-lookup"><span data-stu-id="19174-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="19174-739">Typ danych wyjściowych polecenia cmdlet Set-AzHDInsightGatewaySettings zmieniono z HttpConnectivitySettings na GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="19174-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="19174-740">Dodano kilka przypadków testowych scenariuszy.</span><span class="sxs-lookup"><span data-stu-id="19174-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="19174-741">Usunięto alias: „Add-AzHDInsightConfigValues”, „Get-AzHDInsightProperties”.</span><span class="sxs-lookup"><span data-stu-id="19174-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-742">Az.IotHub</span></span>
* <span data-ttu-id="19174-743">Zmiany powodujące niezgodność:</span><span class="sxs-lookup"><span data-stu-id="19174-743">Breaking changes:</span></span>
    - <span data-ttu-id="19174-744">Polecenie cmdlet „Add-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="19174-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="19174-745">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet Add-AzIotHubEventHubConsumerGroup został usunięty.</span><span class="sxs-lookup"><span data-stu-id="19174-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="19174-746">Polecenie cmdlet „Get-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="19174-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="19174-747">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Get-AzIotHubEventHubConsumerGroup” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="19174-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="19174-748">Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties” została usunięta.</span><span class="sxs-lookup"><span data-stu-id="19174-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="19174-749">Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties” została usunięta.</span><span class="sxs-lookup"><span data-stu-id="19174-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="19174-750">Polecenie cmdlet „New-AzIotHubExportDevice” nie obsługuje już aliasu „New-AzIotHubExportDevices”.</span><span class="sxs-lookup"><span data-stu-id="19174-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="19174-751">Polecenie cmdlet „New-AzIotHubImportDevice” nie obsługuje już aliasu „New-AzIotHubImportDevices”.</span><span class="sxs-lookup"><span data-stu-id="19174-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="19174-752">Polecenie cmdlet „Remove-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="19174-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="19174-753">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Remove-AzIotHubEventHubConsumerGroup” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="19174-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="19174-754">Polecenie cmdlet „Set-AzIotHub” nie obsługuje już parametru „OperationsMonitoringProperties”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="19174-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="19174-755">Zestaw parametrów „UpdateOperationsMonitoringProperties” dla polecenia cmdlet „Set-AzIotHub” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="19174-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-757">Obsługa przez usługę Azure Site Recovery konfigurowania zasobów sieciowych, takich jak sieciowa grupa zabezpieczeń, publiczny adres IP i wewnętrzne moduły równoważenia obciążenia, dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="19174-758">Obsługa przez usługę Azure Site Recovery zapisu na dysku zarządzanym dla odzyskiwania z programu vMWare na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="19174-759">Obsługa przez usługę Azure Site Recovery redukcji karty interfejsu sieciowego dla odzyskiwania z programu vMWare na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="19174-760">Obsługa przez usługę Azure Site Recovery przyspieszonej sieci dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="19174-761">Obsługa przez usługę Azure Site Recovery automatycznej aktualizacji agenta dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="19174-762">Obsługa przez usługę Azure Site Recovery dysku SSD w warstwie Standardowa dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="19174-763">Obsługa przez usługę Azure Site Recovery scenariusza dwuprzebiegowego usługi Azure Disk Encryption dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="19174-764">Obsługa przez usługę Azure Site Recovery ochrony nowo dodanych dysków dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="19174-765">Dodano funkcję SoftDelete dla maszyny wirtualnej i dodano testy dla funkcji softdelete</span><span class="sxs-lookup"><span data-stu-id="19174-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-766">Az.Resources</span></span>
* <span data-ttu-id="19174-767">Aktualizacja zestawu zależnego Microsoft.Extensions.Caching.Memory z 1.1.1 do 2.2</span><span class="sxs-lookup"><span data-stu-id="19174-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-768">Az.Network</span></span>
* <span data-ttu-id="19174-769">Zmieniono wszystkie polecenia cmdlet dla klasy PrivateEndpointConnection w celu obsługi ogólnego dostawcy usług.</span><span class="sxs-lookup"><span data-stu-id="19174-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="19174-770">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="19174-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="19174-776">Dodano nowe polecenie cmdlet dla klasy PrivateLinkResource, które również obsługuje ogólnego dostawcę usług.</span><span class="sxs-lookup"><span data-stu-id="19174-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="19174-777">Nowe polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-777">New cmdlet:</span></span>
        - <span data-ttu-id="19174-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="19174-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="19174-779">Dodano nowe pola i parametr dla funkcji protokołu proxy w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="19174-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="19174-780">Dodano właściwość EnableProxyProtocol w klasie PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="19174-781">Dodano właściwość LinkIdentifier w klasie PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="19174-782">Zaktualizowano polecenie cmdlet New-AzPrivateLinkService w celu dodania nowego opcjonalnego parametru EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="19174-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="19174-783">Poprawiono nieprawidłowy opis parametru w dokumentacji referencyjnej polecenia „New-AzApplicationGatewaySku”</span><span class="sxs-lookup"><span data-stu-id="19174-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="19174-784">Nowe polecenia cmdlet do obsługi zasad usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="19174-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="19174-785">Dodano obsługę zasobu podrzędnego RouteTables klasy VirtualHub</span><span class="sxs-lookup"><span data-stu-id="19174-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="19174-786">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-786">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="19174-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="19174-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="19174-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="19174-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="19174-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="19174-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="19174-792">Dodano obsługę nowych właściwości Sku klasy VirtualHub i VirtualWANType klasy VirtualWan</span><span class="sxs-lookup"><span data-stu-id="19174-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="19174-793">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="19174-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="19174-794">New-AzVirtualHub: dodano parametr Sku</span><span class="sxs-lookup"><span data-stu-id="19174-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="19174-795">Update-AzVirtualHub: dodano parametr Sku</span><span class="sxs-lookup"><span data-stu-id="19174-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="19174-796">New-AzVirtualWan: dodano parametr VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="19174-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="19174-797">Update-AzVirtualWan: dodano parametr VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="19174-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="19174-798">Dodano obsługę właściwości EnableInternetSecurity dla klas HubVnetConnection, VpnConnection i ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="19174-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="19174-799">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-799">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="19174-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="19174-801">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="19174-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="19174-802">New-AzureRmVirtualHubVnetConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="19174-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="19174-803">New-AzureRmVpnConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="19174-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="19174-804">Update-AzureRmVpnConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="19174-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="19174-805">New-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="19174-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="19174-806">Set-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="19174-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="19174-807">Dodano obsługę konfigurowania zasad TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="19174-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="19174-808">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-808">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="19174-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="19174-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="19174-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="19174-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="19174-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="19174-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="19174-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="19174-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="19174-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="19174-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="19174-815">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="19174-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="19174-816">New-AzApplicationGatewayFirewallPolicy: dodano parametr PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="19174-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="19174-817">Dodano obsługę operatora dopasowania geograficznego w obiekcie CustomRule</span><span class="sxs-lookup"><span data-stu-id="19174-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="19174-818">Dodano element GeoMatch do operatora w klasie FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="19174-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="19174-819">Dodano obsługę zasad zapory perListener i perSite</span><span class="sxs-lookup"><span data-stu-id="19174-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="19174-820">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="19174-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="19174-821">New-AzApplicationGatewayHttpListener: dodano parametr FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="19174-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="19174-822">New-AzApplicationGatewayPathRuleConfig: dodano parametr FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="19174-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="19174-823">Poprawka wymaganej podsieci o nazwie AzureBastionSubnet w elemencie „PSBastion” może ignorować wielkość liter</span><span class="sxs-lookup"><span data-stu-id="19174-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="19174-824">Obsługa docelowych nazw FQDN w regułach sieci i przetłumaczonej nazwy FQDN w regułach translatora adresów sieciowych dla usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="19174-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="19174-825">Dodano obsługę zasobu najwyższego poziomu RouteTables klasy IpGroup</span><span class="sxs-lookup"><span data-stu-id="19174-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="19174-826">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-826">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="19174-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="19174-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="19174-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="19174-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="19174-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="19174-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="19174-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-832">Usunięto polecenie cmdlet Add-AzServiceFabricApplicationCertificate, ponieważ ten scenariusz jest objęty poleceniem Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="19174-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-833">Az.Sql</span></span>
* <span data-ttu-id="19174-834">Dodano obsługę przywracania porzuconych baz danych w wystąpieniach zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="19174-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="19174-835">Oznaczono jako przestarzałe w kodzie stare polecenia cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="19174-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="19174-836">Usunięto przestarzałe aliasy:</span><span class="sxs-lookup"><span data-stu-id="19174-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="19174-837">Get-AzSqlDatabaseIndexRecommendations (zamiast tego użyj Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="19174-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="19174-838">Get-AzSqlDatabaseRestorePoints (zamiast tego użyj Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="19174-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="19174-839">Usunięto polecenie cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="19174-840">Usunięto aliasy dla przestarzałych poleceń cmdlet ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="19174-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="19174-841">Oznaczono jako przestarzałe polecenia cmdlet ustawień zaawansowanego wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="19174-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="19174-842">Dodawanie poleceń cmdlet do wyłączania i włączania zaleceń dotyczących czułości dla kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="19174-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-843">Az.Storage</span></span>
* <span data-ttu-id="19174-844">Obsługa włączania dużego udziału plików podczas tworzenia lub aktualizowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="19174-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="19174-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="19174-847">Podczas zamykania/uzyskiwania dojścia do pliku pomiń sprawdzanie, czy ścieżka danych wejściowych jest ścieżką pliku, czy plikiem, aby uniknąć błędu obiektu w stanie DeletePending</span><span class="sxs-lookup"><span data-stu-id="19174-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="19174-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="19174-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="19174-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="19174-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="19174-850">2.8.0 — październik 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="19174-851">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-851">General</span></span>
* <span data-ttu-id="19174-852">Wydanie Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-853">Az.Accounts</span></span>
* <span data-ttu-id="19174-854">Aktualizacja telemetrii i ponowne zapisywanie adresów URL dla wygenerowanych modułów oraz naprawa testów jednostkowych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="19174-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-855">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-856">**Set-AzApiManagementApi** — Dodano obsługę aktualizowania interfejsu API do właściwości ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="19174-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="19174-857">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="19174-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-858">Az.Automation</span></span>
* <span data-ttu-id="19174-859">Naprawiono parametr ponownego uruchamiania polecenia cmdlet New-AzureAutomationSoftwareUpdateConfiguration dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="19174-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="19174-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-860">Az.Batch</span></span>
* <span data-ttu-id="19174-861">Polecenie **Get-AzBatchNodeAgentSku** jest przestarzałe i zostanie zastąpione poleceniem **Get-AzBatchSupportImage** w wersji 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="19174-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-862">Az.Compute</span></span>
* <span data-ttu-id="19174-863">Dodano parametry Priority, EvictionPolicy i MaxPrice do poleceń cmdlet New-AzVM i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="19174-864">Naprawiono komunikat ostrzegawczy i dokumentację pomocy dla poleceń Add-AzVMAdditionalUnattendContent i Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="19174-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="19174-865">Naprawiono wyjątek -skipVmBackup dla maszyn wirtualnych z systemem Linux z dyskami zarządzanymi dla polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="19174-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="19174-866">Naprawiono usterkę w ustawieniach szyfrowania aktualizacji w scenariuszu dwuprzebiegowym polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="19174-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-867">Az.DataFactory</span></span>
* <span data-ttu-id="19174-868">Dodano polecenia CRUD dla przepływu danych usługi ADF w wersji 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow i Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="19174-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="19174-869">Dodano polecenia akcji dla sesji debugowania przepływu danych usługi ADF w wersji 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand i Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="19174-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="19174-870">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.2.0</span><span class="sxs-lookup"><span data-stu-id="19174-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-872">Naprawiono weryfikację kont, aby umożliwić przekazywanie kont ze znakiem „-” bez domeny</span><span class="sxs-lookup"><span data-stu-id="19174-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="19174-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="19174-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="19174-874">Zaktualizowano program PowerShell do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="19174-875">Zaktualizowano zestaw SDK do wersji 1.0.2</span><span class="sxs-lookup"><span data-stu-id="19174-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="19174-876">Zaktualizowano testy, aby odwoływały się do nowej wersji zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="19174-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="19174-877">Zaktualizowano strukturę wyjściową z zagnieżdżonej do spłaszczonej.</span><span class="sxs-lookup"><span data-stu-id="19174-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-878">Az.IotHub</span></span>
* <span data-ttu-id="19174-879">Dodano nowe źródło routingu: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="19174-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="19174-880">Drobna poprawka usterki: Polecenie Get-AzIothub nie zwraca wartości subscriptionId</span><span class="sxs-lookup"><span data-stu-id="19174-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-881">Az.Monitor</span></span>
* <span data-ttu-id="19174-882">Dodano nowe odbiorniki grupy akcji dla grupy akcji -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="19174-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="19174-883">Włączono korzystanie z typowych schematów alertów dla odbiorników.</span><span class="sxs-lookup"><span data-stu-id="19174-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="19174-884">Nie dotyczy to odbiorników wiadomości SMS, powiadomień push usługi Azure App , narzędzia ITSM i połączeń głosowych</span><span class="sxs-lookup"><span data-stu-id="19174-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="19174-885">Elementy webhook obsługują teraz również uwierzytelnianie za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19174-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-886">Az.Network</span></span>
* <span data-ttu-id="19174-887">Dodano nowe polecenie cmdlet Get-AzAvailableServiceAlias, które można wywołać, aby pobrać aliasy do użytku z zasadami punktu końcowego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="19174-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="19174-888">Dodano obsługę dodawania selektorów ruchu do połączeń bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="19174-889">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-889">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="19174-891">Polecenia cmdlet zostały zaktualizowane o opcjonalny parametr -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="19174-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="19174-892">Dodano obsługę protokołów ESP i AH do konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="19174-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="19174-893">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="19174-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="19174-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="19174-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="19174-897">Poprawiono obsługę wyjątków w poleceniach cmdlet usługi Cortex</span><span class="sxs-lookup"><span data-stu-id="19174-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="19174-898">Dodano nowe generacje i jednostki SKU dla elementów VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19174-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="19174-899">Wprowadzono nowe generacje dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="19174-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="19174-900">Wprowadzono nowe jednostki SKU o wysokiej przepływności dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="19174-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="19174-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="19174-901">Az.RedisCache</span></span>
* <span data-ttu-id="19174-902">Zaktualizowano dokumentację referencyjną polecenia „Set-AzRedisCache” w celu uwzględnienia brakujących wartości parametru „-Size”</span><span class="sxs-lookup"><span data-stu-id="19174-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-903">Az.Sql</span></span>
* <span data-ttu-id="19174-904">Dodano obsługę ustawiania administratora usługi Active Directory w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="19174-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-905">Az.Storage</span></span>
* <span data-ttu-id="19174-906">Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 11.1.0</span><span class="sxs-lookup"><span data-stu-id="19174-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="19174-907">Utworzenie listy kontenerów przy użyciu interfejsu API płaszczyzny zarządzania spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="19174-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="19174-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="19174-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="19174-909">Utworzenie listy kont magazynu z subskrypcji spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="19174-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="19174-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="19174-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="19174-911">Az.StorageSync</span></span>
* <span data-ttu-id="19174-912">Naprawiono problem 9810 w poleceniu Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="19174-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-913">Az.Websites</span></span>
* <span data-ttu-id="19174-914">Aktualizowanie elementu ASP aplikacji przy użyciu polecenia Set-AzWebApp kończyło się niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="19174-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="19174-915">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="19174-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-916">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-917">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="19174-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="19174-918">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="19174-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="19174-919">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="19174-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-920">Az.Automation</span></span>
* <span data-ttu-id="19174-921">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="19174-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="19174-922">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="19174-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="19174-923">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="19174-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-924">Az.Compute</span></span>
* <span data-ttu-id="19174-925">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="19174-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="19174-926">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="19174-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="19174-927">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="19174-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="19174-928">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="19174-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="19174-929">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="19174-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="19174-930">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="19174-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="19174-931">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="19174-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="19174-932">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="19174-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="19174-933">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="19174-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-934">Az.DataFactory</span></span>
* <span data-ttu-id="19174-935">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="19174-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="19174-936">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="19174-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-937">Az.HDInsight</span></span>
* <span data-ttu-id="19174-938">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="19174-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-939">Az.IotHub</span></span>
* <span data-ttu-id="19174-940">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="19174-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="19174-941">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="19174-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="19174-942">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-942">New cmdlets are:</span></span>
    - <span data-ttu-id="19174-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="19174-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="19174-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="19174-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="19174-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="19174-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="19174-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="19174-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-947">Az.Monitor</span></span>
* <span data-ttu-id="19174-948">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="19174-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="19174-949">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="19174-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="19174-950">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="19174-951">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="19174-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="19174-952">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="19174-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="19174-953">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="19174-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="19174-954">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="19174-955">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="19174-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="19174-956">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="19174-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="19174-957">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="19174-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="19174-958">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="19174-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="19174-959">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="19174-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="19174-960">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="19174-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="19174-961">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="19174-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="19174-962">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="19174-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="19174-963">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="19174-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="19174-964">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="19174-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="19174-965">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="19174-966">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="19174-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="19174-967">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-967">Overall improved help files</span></span>
* <span data-ttu-id="19174-968">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="19174-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-969">Az.Network</span></span>
* <span data-ttu-id="19174-970">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="19174-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="19174-971">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="19174-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="19174-972">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="19174-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="19174-973">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="19174-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="19174-974">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="19174-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="19174-975">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="19174-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="19174-976">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="19174-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="19174-977">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="19174-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="19174-978">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="19174-979">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="19174-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="19174-980">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="19174-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="19174-981">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="19174-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="19174-982">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-982">New cmdlets</span></span>
        - <span data-ttu-id="19174-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="19174-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="19174-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="19174-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="19174-985">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="19174-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="19174-986">New-VpnSite</span></span>
        - <span data-ttu-id="19174-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="19174-987">Update-VpnSite</span></span>
        - <span data-ttu-id="19174-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="19174-988">New-VpnConnection</span></span>
        - <span data-ttu-id="19174-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="19174-989">Update-VpnConnection</span></span>
* <span data-ttu-id="19174-990">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="19174-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-992">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="19174-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="19174-993">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-994">Az.Resources</span></span>
* <span data-ttu-id="19174-995">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="19174-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-997">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="19174-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="19174-998">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="19174-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="19174-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="19174-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="19174-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="19174-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="19174-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="19174-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="19174-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="19174-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="19174-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="19174-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="19174-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="19174-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="19174-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="19174-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="19174-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="19174-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="19174-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="19174-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="19174-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="19174-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="19174-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="19174-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="19174-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="19174-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="19174-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="19174-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="19174-1012">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="19174-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="19174-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="19174-1013">Az.SignalR</span></span>
* <span data-ttu-id="19174-1014">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="19174-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1015">Az.Sql</span></span>
* <span data-ttu-id="19174-1016">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="19174-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="19174-1017">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="19174-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="19174-1018">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="19174-1019">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="19174-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="19174-1020">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="19174-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1021">Az.Storage</span></span>
* <span data-ttu-id="19174-1022">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="19174-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="19174-1023">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="19174-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="19174-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19174-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="19174-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19174-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="19174-1026">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="19174-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="19174-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="19174-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="19174-1028">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="19174-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="19174-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="19174-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="19174-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="19174-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="19174-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1033">Az.Websites</span></span>
* <span data-ttu-id="19174-1034">Naprawa problemu polegającego na tym, że tagi webapp były usuwane podczas migracji aplikacji do nowej platformy ASP</span><span class="sxs-lookup"><span data-stu-id="19174-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="19174-1035">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="19174-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="19174-1036">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="19174-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="19174-1037">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="19174-1038">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-1038">General</span></span>
* <span data-ttu-id="19174-1039">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="19174-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1040">Az.Accounts</span></span>
* <span data-ttu-id="19174-1041">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="19174-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="19174-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="19174-1042">Az.Aks</span></span>
* <span data-ttu-id="19174-1043">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="19174-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="19174-1044">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="19174-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-1046">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="19174-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="19174-1047">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="19174-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="19174-1048">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="19174-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="19174-1049">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="19174-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="19174-1050">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="19174-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="19174-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-1051">Az.Batch</span></span>
* <span data-ttu-id="19174-1052">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="19174-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-1053">Az.Cdn</span></span>
* <span data-ttu-id="19174-1054">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="19174-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1055">Az.Compute</span></span>
* <span data-ttu-id="19174-1056">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="19174-1057">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="19174-1058">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="19174-1059">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="19174-1060">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="19174-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="19174-1061">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="19174-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="19174-1062">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="19174-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="19174-1063">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="19174-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1064">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1065">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="19174-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="19174-1066">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="19174-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="19174-1067">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="19174-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="19174-1068">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="19174-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1070">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="19174-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-1071">Az.EventHub</span></span>
* <span data-ttu-id="19174-1072">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="19174-1073">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="19174-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="19174-1074">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="19174-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="19174-1075">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="19174-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="19174-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="19174-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="19174-1077">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="19174-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-1078">Az.Monitor</span></span>
* <span data-ttu-id="19174-1079">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1080">Az.Network</span></span>
* <span data-ttu-id="19174-1081">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="19174-1082">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="19174-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="19174-1083">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="19174-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="19174-1084">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="19174-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="19174-1085">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="19174-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="19174-1086">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="19174-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="19174-1087">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="19174-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1089">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="19174-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="19174-1090">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="19174-1090">Added example</span></span>
    - <span data-ttu-id="19174-1091">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="19174-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="19174-1092">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="19174-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="19174-1093">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="19174-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1095">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1096">Az.Resources</span></span>
* <span data-ttu-id="19174-1097">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="19174-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="19174-1098">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="19174-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="19174-1099">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="19174-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="19174-1100">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="19174-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-1102">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="19174-1103">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="19174-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="19174-1104">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="19174-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-1106">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="19174-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="19174-1107">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="19174-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="19174-1108">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="19174-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="19174-1109">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="19174-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="19174-1110">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="19174-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="19174-1111">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="19174-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1112">Az.Sql</span></span>
* <span data-ttu-id="19174-1113">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="19174-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1114">Az.Storage</span></span>
* <span data-ttu-id="19174-1115">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="19174-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="19174-1116">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="19174-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="19174-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="19174-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="19174-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="19174-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="19174-1119">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="19174-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="19174-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="19174-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1121">Az.Websites</span></span>
* <span data-ttu-id="19174-1122">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19174-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="19174-1123">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="19174-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1124">Az.Accounts</span></span>
* <span data-ttu-id="19174-1125">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="19174-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="19174-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="19174-1127">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="19174-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1128">Az.Automation</span></span>
* <span data-ttu-id="19174-1129">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="19174-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-1131">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="19174-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1132">Az.Compute</span></span>
* <span data-ttu-id="19174-1133">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="19174-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19174-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="19174-1135">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="19174-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="19174-1136">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="19174-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1137">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1138">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="19174-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="19174-1139">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="19174-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-1140">Az.EventHub</span></span>
* <span data-ttu-id="19174-1141">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="19174-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="19174-1142">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="19174-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1143">Az.KeyVault</span></span>
* <span data-ttu-id="19174-1144">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="19174-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="19174-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="19174-1145">Az.LogicApp</span></span>
* <span data-ttu-id="19174-1146">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="19174-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="19174-1147">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="19174-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="19174-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="19174-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="19174-1149">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="19174-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1150">Az.Network</span></span>
* <span data-ttu-id="19174-1151">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="19174-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="19174-1152">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1152">New cmdlets</span></span>
        - <span data-ttu-id="19174-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="19174-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="19174-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="19174-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="19174-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="19174-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="19174-1161">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="19174-1162">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="19174-1163">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="19174-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="19174-1164">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="19174-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="19174-1165">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="19174-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="19174-1166">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="19174-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="19174-1167">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="19174-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="19174-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="19174-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="19174-1171">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="19174-1172">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="19174-1173">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="19174-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="19174-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="19174-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="19174-1177">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="19174-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="19174-1178">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="19174-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="19174-1179">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="19174-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1181">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="19174-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="19174-1182">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="19174-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1184">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="19174-1185">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="19174-1186">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="19174-1187">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="19174-1188">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="19174-1189">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="19174-1190">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="19174-1191">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="19174-1192">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="19174-1193">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="19174-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1194">Az.Resources</span></span>
- <span data-ttu-id="19174-1195">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="19174-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="19174-1196">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="19174-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-1198">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="19174-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="19174-1199">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="19174-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1200">Az.Sql</span></span>
* <span data-ttu-id="19174-1201">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="19174-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="19174-1202">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="19174-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="19174-1203">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="19174-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1204">Az.Storage</span></span>
* <span data-ttu-id="19174-1205">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="19174-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="19174-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="19174-1206">Az.StorageSync</span></span>
* <span data-ttu-id="19174-1207">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="19174-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="19174-1208">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="19174-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1209">Az.Websites</span></span>
* <span data-ttu-id="19174-1210">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="19174-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="19174-1211">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="19174-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="19174-1212">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="19174-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="19174-1213">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1214">Az.Accounts</span></span>
* <span data-ttu-id="19174-1215">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="19174-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="19174-1216">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="19174-1217">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="19174-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="19174-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="19174-1218">Az.Advisor</span></span>
* <span data-ttu-id="19174-1219">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="19174-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="19174-1220">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="19174-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="19174-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-1222">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="19174-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="19174-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="19174-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="19174-1224">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="19174-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="19174-1225">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="19174-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="19174-1226">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="19174-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="19174-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="19174-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="19174-1228">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="19174-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1229">Az.Automation</span></span>
* <span data-ttu-id="19174-1230">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="19174-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1231">Az.Compute</span></span>
* <span data-ttu-id="19174-1232">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1233">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1234">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="19174-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="19174-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="19174-1235">Az.EventGrid</span></span>
* <span data-ttu-id="19174-1236">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="19174-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-1237">Az.IotHub</span></span>
* <span data-ttu-id="19174-1238">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="19174-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1239">Az.Network</span></span>
* <span data-ttu-id="19174-1240">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="19174-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="19174-1241">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="19174-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-1243">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="19174-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="19174-1244">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="19174-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1246">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="19174-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1248">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="19174-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1249">Az.Resources</span></span>
    - <span data-ttu-id="19174-1250">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="19174-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="19174-1251">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="19174-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="19174-1252">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="19174-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="19174-1253">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="19174-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-1255">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="19174-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1256">Az.Sql</span></span>
* <span data-ttu-id="19174-1257">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="19174-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="19174-1258">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="19174-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="19174-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="19174-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="19174-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="19174-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="19174-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="19174-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="19174-1265">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="19174-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1266">Az.Storage</span></span>
* <span data-ttu-id="19174-1267">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="19174-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="19174-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="19174-1269">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="19174-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="19174-1270">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="19174-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="19174-1271">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="19174-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="19174-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="19174-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="19174-1274">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="19174-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="19174-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="19174-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="19174-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="19174-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="19174-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="19174-1277">Az.StorageSync</span></span>
* <span data-ttu-id="19174-1278">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="19174-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="19174-1279">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1280">Az.Accounts</span></span>
* <span data-ttu-id="19174-1281">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="19174-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="19174-1282">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="19174-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="19174-1283">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="19174-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="19174-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="19174-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="19174-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="19174-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1286">Az.Compute</span></span>
* <span data-ttu-id="19174-1287">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="19174-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="19174-1288">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="19174-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="19174-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="19174-1289">Az.Dns</span></span>
* <span data-ttu-id="19174-1290">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="19174-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="19174-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="19174-1291">Az.EventGrid</span></span>
* <span data-ttu-id="19174-1292">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="19174-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="19174-1293">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1293">New cmdlets:</span></span>
    - <span data-ttu-id="19174-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="19174-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="19174-1295">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="19174-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="19174-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="19174-1297">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="19174-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="19174-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="19174-1299">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="19174-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="19174-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="19174-1301">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="19174-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="19174-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="19174-1303">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="19174-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="19174-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="19174-1305">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="19174-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="19174-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="19174-1307">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="19174-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="19174-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="19174-1309">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="19174-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="19174-1310">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="19174-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="19174-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="19174-1312">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="19174-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="19174-1313">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="19174-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="19174-1314">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="19174-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="19174-1315">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="19174-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="19174-1316">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="19174-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="19174-1317">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="19174-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="19174-1318">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="19174-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="19174-1319">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="19174-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="19174-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="19174-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="19174-1321">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="19174-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="19174-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="19174-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="19174-1323">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="19174-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="19174-1324">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="19174-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="19174-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="19174-1327">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="19174-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="19174-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="19174-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="19174-1329">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="19174-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1330">Az.Network</span></span>
* <span data-ttu-id="19174-1331">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="19174-1332">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1332">New cmdlets</span></span>
        - <span data-ttu-id="19174-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="19174-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="19174-1334">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="19174-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="19174-1335">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1335">New cmdlets</span></span>
        - <span data-ttu-id="19174-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="19174-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="19174-1337">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="19174-1338">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1338">New cmdlets</span></span>
        - <span data-ttu-id="19174-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="19174-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="19174-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19174-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="19174-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="19174-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="19174-1344">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="19174-1345">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1345">New cmdlets</span></span>
        - <span data-ttu-id="19174-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="19174-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="19174-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="19174-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="19174-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="19174-1350">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="19174-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="19174-1351">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="19174-1352">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="19174-1353">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="19174-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="19174-1354">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="19174-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="19174-1355">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="19174-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="19174-1356">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="19174-1357">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="19174-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="19174-1358">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="19174-1359">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="19174-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="19174-1360">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="19174-1361">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="19174-1362">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="19174-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="19174-1363">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="19174-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="19174-1364">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="19174-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="19174-1365">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="19174-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="19174-1366">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="19174-1367">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="19174-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="19174-1368">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="19174-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="19174-1369">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19174-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="19174-1370">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="19174-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="19174-1371">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="19174-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="19174-1372">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="19174-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1374">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="19174-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1375">Az.Resources</span></span>
* <span data-ttu-id="19174-1376">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="19174-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="19174-1377">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="19174-1378">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="19174-1379">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="19174-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-1381">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="19174-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1382">Az.Sql</span></span>
* <span data-ttu-id="19174-1383">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="19174-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="19174-1384">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="19174-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="19174-1385">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="19174-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="19174-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19174-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="19174-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19174-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="19174-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19174-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="19174-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="19174-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="19174-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="19174-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1391">Az.Storage</span></span>
* <span data-ttu-id="19174-1392">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="19174-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="19174-1394">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="19174-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="19174-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1396">Az.Websites</span></span>
* <span data-ttu-id="19174-1397">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="19174-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="19174-1398">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="19174-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="19174-1399">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="19174-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-1400">Az.Cdn</span></span>
* <span data-ttu-id="19174-1401">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="19174-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1402">Az.Compute</span></span>
* <span data-ttu-id="19174-1403">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="19174-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="19174-1404">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="19174-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-1405">Az.EventHub</span></span>
* <span data-ttu-id="19174-1406">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="19174-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="19174-1407">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19174-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1408">Az.Network</span></span>
* <span data-ttu-id="19174-1409">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="19174-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="19174-1410">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="19174-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-1412">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="19174-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1414">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="19174-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-1416">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19174-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-1418">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="19174-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="19174-1419">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="19174-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1420">Az.Sql</span></span>
* <span data-ttu-id="19174-1421">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19174-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="19174-1422">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="19174-1423">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="19174-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="19174-1424">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="19174-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1425">Az.Websites</span></span>
* <span data-ttu-id="19174-1426">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="19174-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="19174-1427">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="19174-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-1429">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="19174-1430">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="19174-1431">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="19174-1432">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="19174-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="19174-1433">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="19174-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="19174-1434">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="19174-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="19174-1435">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="19174-1436">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="19174-1437">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="19174-1438">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="19174-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="19174-1439">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="19174-1440">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="19174-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="19174-1441">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="19174-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="19174-1442">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="19174-1443">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="19174-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="19174-1444">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="19174-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="19174-1445">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="19174-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="19174-1446">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="19174-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="19174-1447">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="19174-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="19174-1448">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="19174-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="19174-1449">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="19174-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="19174-1450">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="19174-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="19174-1451">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="19174-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="19174-1452">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="19174-1453">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="19174-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="19174-1454">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="19174-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="19174-1455">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="19174-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="19174-1456">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="19174-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="19174-1457">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="19174-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="19174-1458">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="19174-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="19174-1459">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="19174-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="19174-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="19174-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="19174-1461">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="19174-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="19174-1462">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="19174-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="19174-1463">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="19174-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="19174-1464">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="19174-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="19174-1465">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="19174-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="19174-1466">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="19174-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="19174-1467">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="19174-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="19174-1468">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="19174-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="19174-1469">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="19174-1470">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="19174-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="19174-1471">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="19174-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="19174-1472">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="19174-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="19174-1473">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="19174-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="19174-1474">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="19174-1475">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="19174-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="19174-1476">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="19174-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="19174-1477">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="19174-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="19174-1478">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="19174-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="19174-1479">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="19174-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="19174-1480">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="19174-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="19174-1481">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="19174-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="19174-1482">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="19174-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="19174-1483">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="19174-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="19174-1484">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="19174-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="19174-1485">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="19174-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="19174-1486">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="19174-1487">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="19174-1488">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="19174-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="19174-1489">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="19174-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="19174-1490">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="19174-1491">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="19174-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="19174-1492">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="19174-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="19174-1493">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="19174-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="19174-1494">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="19174-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="19174-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="19174-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="19174-1496">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="19174-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="19174-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="19174-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="19174-1498">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="19174-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="19174-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="19174-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="19174-1500">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="19174-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="19174-1501">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="19174-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="19174-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="19174-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="19174-1503">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="19174-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="19174-1504">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="19174-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="19174-1505">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="19174-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1506">Az.Automation</span></span>
* <span data-ttu-id="19174-1507">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="19174-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="19174-1508">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="19174-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="19174-1509">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="19174-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="19174-1510">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="19174-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="19174-1511">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="19174-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="19174-1512">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="19174-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="19174-1513">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="19174-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1514">Az.Compute</span></span>
* <span data-ttu-id="19174-1515">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="19174-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="19174-1516">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="19174-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1518">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-1519">Az.Monitor</span></span>
* <span data-ttu-id="19174-1520">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1521">Az.Network</span></span>
* <span data-ttu-id="19174-1522">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="19174-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="19174-1523">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="19174-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="19174-1525">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="19174-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1526">Az.Resources</span></span>
* <span data-ttu-id="19174-1527">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="19174-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1528">Az.Sql</span></span>
* <span data-ttu-id="19174-1529">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="19174-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="19174-1530">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1531">Az.Accounts</span></span>
* <span data-ttu-id="19174-1532">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="19174-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-1534">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="19174-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="19174-1535">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="19174-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1536">Az.Compute</span></span>
* <span data-ttu-id="19174-1537">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="19174-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="19174-1538">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="19174-1539">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="19174-1540">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="19174-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="19174-1541">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="19174-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="19174-1542">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="19174-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="19174-1543">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="19174-1543">Breaking changes</span></span>
    - <span data-ttu-id="19174-1544">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="19174-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="19174-1545">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="19174-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="19174-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="19174-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="19174-1547">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="19174-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="19174-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="19174-1548">Az.Dns</span></span>
* <span data-ttu-id="19174-1549">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="19174-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="19174-1550">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="19174-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="19174-1551">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="19174-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="19174-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="19174-1553">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="19174-1554">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="19174-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="19174-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-1555">Az.HDInsight</span></span>
* <span data-ttu-id="19174-1556">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="19174-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19174-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="19174-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19174-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="19174-1559">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19174-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="19174-1560">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="19174-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="19174-1561">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="19174-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="19174-1562">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="19174-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-1563">Az.Monitor</span></span>
* <span data-ttu-id="19174-1564">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="19174-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="19174-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="19174-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="19174-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="19174-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="19174-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="19174-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="19174-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="19174-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="19174-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="19174-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="19174-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="19174-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19174-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="19174-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19174-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="19174-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19174-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="19174-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19174-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="19174-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19174-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="19174-1576">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="19174-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="19174-1577">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="19174-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1578">Az.Network</span></span>
* <span data-ttu-id="19174-1579">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="19174-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="19174-1580">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1580">New cmdlets</span></span>
        - <span data-ttu-id="19174-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="19174-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="19174-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="19174-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="19174-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="19174-1585">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="19174-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="19174-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="19174-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="19174-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="19174-1588">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="19174-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="19174-1589">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="19174-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="19174-1590">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="19174-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-1592">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="19174-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="19174-1593">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="19174-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="19174-1594">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="19174-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1596">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="19174-1597">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="19174-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="19174-1598">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="19174-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="19174-1599">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="19174-1600">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19174-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="19174-1601">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="19174-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="19174-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="19174-1602">Az.Relay</span></span>
* <span data-ttu-id="19174-1603">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="19174-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-1605">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="19174-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1606">Az.Storage</span></span>
* <span data-ttu-id="19174-1607">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="19174-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="19174-1608">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="19174-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="19174-1609">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="19174-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="19174-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="19174-1611">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="19174-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="19174-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="19174-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="19174-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1615">Az.Websites</span></span>
* <span data-ttu-id="19174-1616">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="19174-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="19174-1617">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="19174-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="19174-1618">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-1619">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-1620">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="19174-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="19174-1621">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="19174-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="19174-1622">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="19174-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="19174-1623">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="19174-1624">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="19174-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="19174-1625">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="19174-1626">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1627">Az.Accounts</span></span>
* <span data-ttu-id="19174-1628">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="19174-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="19174-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-1629">Az.Batch</span></span>
* <span data-ttu-id="19174-1630">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-1631">Az.Cdn</span></span>
* <span data-ttu-id="19174-1632">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-1634">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1635">Az.Compute</span></span>
* <span data-ttu-id="19174-1636">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="19174-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="19174-1637">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1638">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1639">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1640">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="19174-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1642">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="19174-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="19174-1643">Az.EventGrid</span></span>
* <span data-ttu-id="19174-1644">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="19174-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-1645">Az.EventHub</span></span>
* <span data-ttu-id="19174-1646">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="19174-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="19174-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="19174-1647">Az.HDInsight</span></span>
* <span data-ttu-id="19174-1648">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-1649">Az.IotHub</span></span>
* <span data-ttu-id="19174-1650">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1651">Az.KeyVault</span></span>
* <span data-ttu-id="19174-1652">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1653">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="19174-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="19174-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="19174-1655">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="19174-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="19174-1656">Az.Media</span></span>
* <span data-ttu-id="19174-1657">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-1658">Az.Monitor</span></span>
  * <span data-ttu-id="19174-1659">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="19174-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="19174-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="19174-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="19174-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="19174-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="19174-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="19174-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="19174-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="19174-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="19174-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="19174-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="19174-1665">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="19174-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1666">Az.Network</span></span>
* <span data-ttu-id="19174-1667">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1668">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="19174-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="19174-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="19174-1670">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1672">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="19174-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="19174-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="19174-1674">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1676">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1677">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="19174-1678">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="19174-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="19174-1679">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="19174-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="19174-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="19174-1680">Az.RedisCache</span></span>
* <span data-ttu-id="19174-1681">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1682">Az.Resources</span></span>
* <span data-ttu-id="19174-1683">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1684">Az.Sql</span></span>
* <span data-ttu-id="19174-1685">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="19174-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="19174-1686">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1687">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="19174-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="19174-1688">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="19174-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="19174-1689">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="19174-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="19174-1690">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19174-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="19174-1691">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1692">Az.Websites</span></span>
* <span data-ttu-id="19174-1693">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="19174-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="19174-1694">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="19174-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="19174-1695">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="19174-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="19174-1696">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="19174-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="19174-1697">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-1698">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-1699">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="19174-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="19174-1700">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="19174-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="19174-1701">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="19174-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="19174-1702">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="19174-1703">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="19174-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="19174-1704">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="19174-1705">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="19174-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1706">Az.Accounts</span></span>
* <span data-ttu-id="19174-1707">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19174-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="19174-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="19174-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="19174-1709">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="19174-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="19174-1710">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="19174-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1711">Az.Automation</span></span>
* <span data-ttu-id="19174-1712">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="19174-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="19174-1713">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="19174-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="19174-1714">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1715">Az.Compute</span></span>
* <span data-ttu-id="19174-1716">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="19174-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="19174-1717">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="19174-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="19174-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="19174-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="19174-1719">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="19174-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1720">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1721">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="19174-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="19174-1722">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="19174-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1723">Az.Resources</span></span>
* <span data-ttu-id="19174-1724">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="19174-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="19174-1725">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="19174-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="19174-1726">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="19174-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="19174-1727">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="19174-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="19174-1728">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="19174-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="19174-1729">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="19174-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1730">Az.Sql</span></span>
* <span data-ttu-id="19174-1731">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="19174-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1732">Az.Storage</span></span>
* <span data-ttu-id="19174-1733">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="19174-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19174-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="19174-1735">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="19174-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="19174-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="19174-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="19174-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="19174-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="19174-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="19174-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="19174-1740">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="19174-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="19174-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="19174-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="19174-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="19174-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="19174-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19174-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="19174-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19174-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="19174-1745">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="19174-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="19174-1746">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="19174-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="19174-1747">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="19174-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="19174-1748">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="19174-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="19174-1749">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="19174-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="19174-1750">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="19174-1751">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="19174-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="19174-1752">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="19174-1753">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1754">Az.Automation</span></span>
* <span data-ttu-id="19174-1755">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="19174-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="19174-1756">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="19174-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="19174-1757">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="19174-1757">Pre-Post script</span></span>
    * <span data-ttu-id="19174-1758">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="19174-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1759">Az.Compute</span></span>
* <span data-ttu-id="19174-1760">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="19174-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="19174-1761">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="19174-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1762">Az.KeyVault</span></span>
* <span data-ttu-id="19174-1763">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1764">Az.Network</span></span>
* <span data-ttu-id="19174-1765">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="19174-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="19174-1766">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="19174-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1768">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="19174-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="19174-1769">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="19174-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1770">Az.Resources</span></span>
* <span data-ttu-id="19174-1771">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19174-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="19174-1772">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="19174-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1773">Az.Sql</span></span>
* <span data-ttu-id="19174-1774">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="19174-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1775">Az.Storage</span></span>
* <span data-ttu-id="19174-1776">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="19174-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="19174-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="19174-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="19174-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="19174-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="19174-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="19174-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="19174-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="19174-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1783">Az.Websites</span></span>
* <span data-ttu-id="19174-1784">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="19174-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="19174-1785">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="19174-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1786">Az.Accounts</span></span>
* <span data-ttu-id="19174-1787">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="19174-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="19174-1788">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1789">Az.Automation</span></span>
* <span data-ttu-id="19174-1790">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="19174-1791">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="19174-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="19174-1792">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="19174-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-1793">Az.Cdn</span></span>
* <span data-ttu-id="19174-1794">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="19174-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1795">Az.Compute</span></span>
* <span data-ttu-id="19174-1796">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="19174-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1797">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1798">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="19174-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="19174-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="19174-1799">Az.LogicApp</span></span>
* <span data-ttu-id="19174-1800">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="19174-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1801">Az.Network</span></span>
* <span data-ttu-id="19174-1802">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="19174-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1804">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="19174-1805">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="19174-1805">SDK Update</span></span>
* <span data-ttu-id="19174-1806">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="19174-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="19174-1807">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="19174-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1808">Az.Resources</span></span>
* <span data-ttu-id="19174-1809">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="19174-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="19174-1810">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="19174-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="19174-1811">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="19174-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="19174-1812">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="19174-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="19174-1813">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="19174-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="19174-1814">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="19174-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1815">Az.Sql</span></span>
* <span data-ttu-id="19174-1816">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="19174-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="19174-1817">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="19174-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1818">Az.Storage</span></span>
* <span data-ttu-id="19174-1819">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="19174-1820">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="19174-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="19174-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="19174-1822">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="19174-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1823">Az.Automation</span></span>
* <span data-ttu-id="19174-1824">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="19174-1825">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="19174-1826">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-1828">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="19174-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1829">Az.Compute</span></span>
* <span data-ttu-id="19174-1830">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="19174-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="19174-1831">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="19174-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="19174-1832">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="19174-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="19174-1833">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="19174-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1835">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="19174-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="19174-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="19174-1836">Az.EventHub</span></span>
* <span data-ttu-id="19174-1837">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="19174-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1838">Az.KeyVault</span></span>
* <span data-ttu-id="19174-1839">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19174-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="19174-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="19174-1840">Az.LogicApp</span></span>
* <span data-ttu-id="19174-1841">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="19174-1842">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="19174-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="19174-1843">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="19174-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="19174-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="19174-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="19174-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="19174-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="19174-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="19174-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="19174-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="19174-1848">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="19174-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="19174-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="19174-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="19174-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="19174-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="19174-1853">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="19174-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="19174-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-1854">Az.Monitor</span></span>
* <span data-ttu-id="19174-1855">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="19174-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1856">Az.Network</span></span>
* <span data-ttu-id="19174-1857">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="19174-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="19174-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="19174-1859">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="19174-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="19174-1860">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="19174-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="19174-1861">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="19174-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1862">Az.Resources</span></span>
* <span data-ttu-id="19174-1863">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="19174-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="19174-1864">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="19174-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="19174-1865">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="19174-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="19174-1866">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="19174-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1867">Az.Sql</span></span>
* <span data-ttu-id="19174-1868">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="19174-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="19174-1869">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="19174-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1870">Az.Websites</span></span>
* <span data-ttu-id="19174-1871">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="19174-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="19174-1872">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1873">Az.Accounts</span></span>
* <span data-ttu-id="19174-1874">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="19174-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="19174-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="19174-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="19174-1876">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="19174-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1877">Az.Compute</span></span>
* <span data-ttu-id="19174-1878">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="19174-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="19174-1879">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="19174-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="19174-1880">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="19174-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="19174-1882">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="19174-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1883">Az.Resources</span></span>
* <span data-ttu-id="19174-1884">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="19174-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="19174-1885">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="19174-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="19174-1886">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="19174-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="19174-1887">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="19174-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1888">Az.Sql</span></span>
* <span data-ttu-id="19174-1889">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="19174-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="19174-1890">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="19174-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="19174-1891">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="19174-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="19174-1892">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1893">Az.Accounts</span></span>
* <span data-ttu-id="19174-1894">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="19174-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="19174-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="19174-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="19174-1896">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="19174-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="19174-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="19174-1898">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="19174-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="19174-1899">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1900">Az.Accounts</span></span>
* <span data-ttu-id="19174-1901">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="19174-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="19174-1902">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="19174-1903">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="19174-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="19174-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="19174-1904">Az.Aks</span></span>
* <span data-ttu-id="19174-1905">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="19174-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-1906">Az.Automation</span></span>
* <span data-ttu-id="19174-1907">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="19174-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="19174-1908">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="19174-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="19174-1909">Az.Cdn</span></span>
* <span data-ttu-id="19174-1910">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1911">Az.Compute</span></span>
* <span data-ttu-id="19174-1912">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="19174-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="19174-1913">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19174-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="19174-1914">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="19174-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="19174-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19174-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="19174-1916">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="19174-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19174-1917">Az.DataFactory</span></span>
* <span data-ttu-id="19174-1918">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="19174-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1920">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="19174-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="19174-1921">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="19174-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="19174-1922">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-1923">Az.IotHub</span></span>
* <span data-ttu-id="19174-1924">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="19174-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="19174-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-1925">Az.KeyVault</span></span>
* <span data-ttu-id="19174-1926">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-1927">Az.Network</span></span>
* <span data-ttu-id="19174-1928">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1929">Az.Resources</span></span>
* <span data-ttu-id="19174-1930">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="19174-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="19174-1931">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="19174-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="19174-1932">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19174-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="19174-1933">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="19174-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="19174-1934">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="19174-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="19174-1935">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="19174-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="19174-1936">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="19174-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-1938">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="19174-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="19174-1939">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="19174-1939">Fix some error messages.</span></span>
* <span data-ttu-id="19174-1940">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="19174-1941">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="19174-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="19174-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="19174-1942">Az.SignalR</span></span>
* <span data-ttu-id="19174-1943">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1944">Az.Sql</span></span>
* <span data-ttu-id="19174-1945">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="19174-1946">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="19174-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="19174-1947">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="19174-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="19174-1948">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="19174-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1949">Az.Storage</span></span>
* <span data-ttu-id="19174-1950">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="19174-1951">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="19174-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="19174-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="19174-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="19174-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="19174-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="19174-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="19174-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="19174-1955">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-1956">Az.Websites</span></span>
* <span data-ttu-id="19174-1957">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="19174-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="19174-1958">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="19174-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="19174-1959">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="19174-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="19174-1960">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="19174-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="19174-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1961">Az.Accounts</span></span>
* <span data-ttu-id="19174-1962">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="19174-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-1963">Az.Compute</span></span>
* <span data-ttu-id="19174-1964">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="19174-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="19174-1965">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="19174-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="19174-1966">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-1968">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="19174-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="19174-1969">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="19174-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="19174-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="19174-1970">Az.EventGrid</span></span>
* <span data-ttu-id="19174-1971">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="19174-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="19174-1972">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="19174-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="19174-1973">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="19174-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="19174-1974">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="19174-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="19174-1975">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="19174-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="19174-1976">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="19174-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="19174-1977">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="19174-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="19174-1978">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="19174-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="19174-1979">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="19174-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="19174-1980">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="19174-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="19174-1981">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="19174-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="19174-1982">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="19174-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="19174-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-1983">Az.IotHub</span></span>
* <span data-ttu-id="19174-1984">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="19174-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="19174-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="19174-1985">Az.LogicApp</span></span>
* <span data-ttu-id="19174-1986">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="19174-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-1987">Az.Resources</span></span>
* <span data-ttu-id="19174-1988">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="19174-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="19174-1989">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="19174-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="19174-1990">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19174-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="19174-1991">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="19174-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="19174-1992">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="19174-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="19174-1993">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="19174-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="19174-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="19174-1994">Az.SignalR</span></span>
* <span data-ttu-id="19174-1995">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-1996">Az.Sql</span></span>
* <span data-ttu-id="19174-1997">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="19174-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="19174-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-1998">Az.Storage</span></span>
* <span data-ttu-id="19174-1999">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="19174-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="19174-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19174-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="19174-2001">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="19174-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="19174-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="19174-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-2003">Az.Websites</span></span>
* <span data-ttu-id="19174-2004">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="19174-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="19174-2005">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="19174-2006">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="19174-2007">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-2007">General</span></span>

- <span data-ttu-id="19174-2008">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="19174-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="19174-2009">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="19174-2009">Online help for each module</span></span>
- <span data-ttu-id="19174-2010">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="19174-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="19174-2011">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="19174-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="19174-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-2012">Az.Accounts</span></span>
- <span data-ttu-id="19174-2013">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="19174-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="19174-2014">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="19174-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="19174-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="19174-2016">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="19174-2016">Fixes for #7002</span></span>
- <span data-ttu-id="19174-2017">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="19174-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="19174-2018">Az.Batch</span></span>
- <span data-ttu-id="19174-2019">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="19174-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="19174-2020">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="19174-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="19174-2021">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="19174-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="19174-2022">Az.Billing</span></span>
- <span data-ttu-id="19174-2023">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="19174-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="19174-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="19174-2025">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="19174-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="19174-2026">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="19174-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="19174-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="19174-2028">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="19174-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="19174-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="19174-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="19174-2030">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="19174-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="19174-2032">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="19174-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="19174-2033">Az.Monitor</span></span>
- <span data-ttu-id="19174-2034">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="19174-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="19174-2035">Az.KeyVault</span></span>
- <span data-ttu-id="19174-2036">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="19174-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="19174-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="19174-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="19174-2038">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="19174-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="19174-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="19174-2039">Az.Media</span></span>
- <span data-ttu-id="19174-2040">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="19174-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="19174-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-2041">Az.Network</span></span>
<span data-ttu-id="19174-2042">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="19174-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="19174-2043">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="19174-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="19174-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="19174-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="19174-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="19174-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="19174-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="19174-2052">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="19174-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="19174-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19174-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="19174-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="19174-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="19174-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="19174-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="19174-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19174-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="19174-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="19174-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="19174-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="19174-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="19174-2059">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19174-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="19174-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19174-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="19174-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19174-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="19174-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19174-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="19174-2063">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="19174-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="19174-2064">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="19174-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="19174-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="19174-2066">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="19174-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="19174-2067">Az.Profile</span></span>
- <span data-ttu-id="19174-2068">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="19174-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="19174-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="19174-2070">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="19174-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2071">Az.Resources</span></span>
- <span data-ttu-id="19174-2072">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="19174-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="19174-2074">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="19174-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="19174-2075">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="19174-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="19174-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="19174-2077">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="19174-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="19174-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-2078">Az.Sql</span></span>
- <span data-ttu-id="19174-2079">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="19174-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="19174-2080">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="19174-2081">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="19174-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-2082">Az.Storage</span></span>
- <span data-ttu-id="19174-2083">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="19174-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-2084">Az.Websites</span></span>
- <span data-ttu-id="19174-2085">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="19174-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="19174-2086">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="19174-2087">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-2087">General</span></span>

* <span data-ttu-id="19174-2088">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="19174-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="19174-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-2089">Az.Compute</span></span>

* <span data-ttu-id="19174-2090">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="19174-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="19174-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="19174-2092">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="19174-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="19174-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="19174-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="19174-2094">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="19174-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="19174-2095">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="19174-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="19174-2096">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="19174-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="19174-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="19174-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="19174-2098">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="19174-2099">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19174-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="19174-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2100">Az.Resources</span></span>

* <span data-ttu-id="19174-2101">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="19174-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="19174-2102">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="19174-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="19174-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-2103">Az.Sql</span></span>

* <span data-ttu-id="19174-2104">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="19174-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="19174-2105">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="19174-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="19174-2106">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="19174-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="19174-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-2107">Az.Storage</span></span>

* <span data-ttu-id="19174-2108">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19174-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="19174-2109">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="19174-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="19174-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="19174-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="19174-2111">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="19174-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="19174-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="19174-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="19174-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="19174-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="19174-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-2114">Az.Websites</span></span>

* <span data-ttu-id="19174-2115">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19174-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="19174-2116">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="19174-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="19174-2117">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="19174-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="19174-2118">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="19174-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="19174-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="19174-2120">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="19174-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="19174-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="19174-2121">Az.Automation</span></span>
* <span data-ttu-id="19174-2122">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="19174-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="19174-2123">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="19174-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="19174-2124">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="19174-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="19174-2125">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="19174-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="19174-2126">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="19174-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="19174-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-2127">Az.Compute</span></span>
* <span data-ttu-id="19174-2128">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="19174-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="19174-2129">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="19174-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="19174-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="19174-2131">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="19174-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="19174-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="19174-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="19174-2133">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="19174-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="19174-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-2134">Az.Network</span></span>
* <span data-ttu-id="19174-2135">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="19174-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="19174-2136">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="19174-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="19174-2137">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="19174-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="19174-2138">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19174-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="19174-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="19174-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="19174-2140">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="19174-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="19174-2141">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="19174-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="19174-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="19174-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="19174-2143">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="19174-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="19174-2144">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="19174-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="19174-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="19174-2145">Az.Relay</span></span>
* <span data-ttu-id="19174-2146">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="19174-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="19174-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2147">Az.Resources</span></span>
* <span data-ttu-id="19174-2148">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="19174-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="19174-2149">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="19174-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="19174-2150">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="19174-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="19174-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-2152">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="19174-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="19174-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-2153">Az.Sql</span></span>
* <span data-ttu-id="19174-2154">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="19174-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="19174-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="19174-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="19174-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="19174-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="19174-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="19174-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="19174-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="19174-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="19174-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="19174-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="19174-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="19174-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="19174-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="19174-2163">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="19174-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="19174-2164">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="19174-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="19174-2165">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="19174-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="19174-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="19174-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="19174-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="19174-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="19174-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="19174-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="19174-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="19174-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="19174-2170">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="19174-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="19174-2171">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="19174-2172">Ogólne</span><span class="sxs-lookup"><span data-stu-id="19174-2172">General</span></span>
* <span data-ttu-id="19174-2173">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="19174-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="19174-2174">Az.Profile</span></span>
* <span data-ttu-id="19174-2175">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="19174-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="19174-2176">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="19174-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="19174-2177">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="19174-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="19174-2178">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="19174-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="19174-2179">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="19174-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="19174-2180">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="19174-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="19174-2181">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="19174-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-2183">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="19174-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-2184">Az.Compute</span></span>
* <span data-ttu-id="19174-2185">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="19174-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="19174-2186">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="19174-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="19174-2187">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="19174-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-2189">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="19174-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="19174-2190">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="19174-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="19174-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="19174-2191">Az.Insights</span></span>
* <span data-ttu-id="19174-2192">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="19174-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="19174-2193">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="19174-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="19174-2194">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="19174-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="19174-2195">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="19174-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-2196">Az.Network</span></span>
* <span data-ttu-id="19174-2197">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="19174-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="19174-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="19174-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="19174-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="19174-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="19174-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="19174-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="19174-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="19174-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="19174-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="19174-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="19174-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="19174-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="19174-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="19174-2205">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="19174-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2206">Az.Resources</span></span>
* <span data-ttu-id="19174-2207">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="19174-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="19174-2208">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="19174-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="19174-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="19174-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="19174-2210">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="19174-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="19174-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="19174-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="19174-2212">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="19174-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="19174-2213">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="19174-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="19174-2214">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="19174-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="19174-2215">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="19174-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="19174-2216">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="19174-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="19174-2217">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="19174-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="19174-2218">Az.Profile</span></span>
* <span data-ttu-id="19174-2219">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="19174-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="19174-2220">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="19174-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-2221">Az.Compute</span></span>
* <span data-ttu-id="19174-2222">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="19174-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="19174-2223">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="19174-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="19174-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="19174-2225">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19174-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="19174-2226">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19174-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="19174-2227">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19174-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="19174-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19174-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="19174-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19174-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-2230">Az.Network</span></span>
* <span data-ttu-id="19174-2231">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="19174-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="19174-2232">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19174-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2233">Az.Resources</span></span>
* <span data-ttu-id="19174-2234">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="19174-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="19174-2235">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="19174-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="19174-2236">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="19174-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="19174-2237">Azure.Storage</span></span>
* <span data-ttu-id="19174-2238">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="19174-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="19174-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="19174-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="19174-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="19174-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="19174-2241">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="19174-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="19174-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="19174-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="19174-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="19174-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="19174-2244">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="19174-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="19174-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="19174-2245">Az.Compute</span></span>
* <span data-ttu-id="19174-2246">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="19174-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="19174-2247">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="19174-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="19174-2248">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="19174-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="19174-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="19174-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="19174-2250">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="19174-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="19174-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="19174-2251">Az.Network</span></span>
* <span data-ttu-id="19174-2252">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="19174-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="19174-2253">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="19174-2253">new cmdlets added</span></span>
    - <span data-ttu-id="19174-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="19174-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="19174-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="19174-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="19174-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="19174-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="19174-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="19174-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="19174-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="19174-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="19174-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="19174-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="19174-2260">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="19174-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="19174-2261">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="19174-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="19174-2262">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="19174-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="19174-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="19174-2263">Az.RedisCache</span></span>
* <span data-ttu-id="19174-2264">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="19174-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="19174-2265">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="19174-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="19174-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="19174-2266">Az.Resources</span></span>
* <span data-ttu-id="19174-2267">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19174-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="19174-2268">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="19174-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="19174-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="19174-2269">Az.Sql</span></span>
* <span data-ttu-id="19174-2270">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="19174-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="19174-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="19174-2271">Az.Websites</span></span>
* <span data-ttu-id="19174-2272">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="19174-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="19174-2273">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="19174-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="19174-2274">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="19174-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="19174-2275">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="19174-2275">Initial Release</span></span>
