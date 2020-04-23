---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740545"
---
## <a name="380---april-2020"></a><span data-ttu-id="097f4-103">3.8.0 — kwiecień 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-104">Az.Accounts</span></span>
* <span data-ttu-id="097f4-105">Zaktualizowano adres URL ankiety Azure PowerShell w poleceniu „Resolve-AzError” [nr 11507]</span><span class="sxs-lookup"><span data-stu-id="097f4-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-106">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-107">Dodano powiadomienie o zmianie powodującej niezgodność dotyczącej danych wyjściowych poleceń cmdlet dla plików platformy Azure, która zostanie wprowadzona w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="097f4-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="097f4-108">Zaktualizowano dokumentację polecenia „Set-AzApiManagementGroup” w celu określenia parametru GroupId</span><span class="sxs-lookup"><span data-stu-id="097f4-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-109">Az.Cdn</span></span>
* <span data-ttu-id="097f4-110">Poprawiono wyświetlanie jednostek SKU z cenami dotyczącymi sieci ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="097f4-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-112">Dodano obsługę elementów Identity, Encryption i UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="097f4-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="097f4-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-113">Az.Compute</span></span>
* <span data-ttu-id="097f4-114">Dodano polecenie cmdlet „Set-AzVmssOrchestrationServiceState”.</span><span class="sxs-lookup"><span data-stu-id="097f4-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="097f4-115">Polecenie „Get-AzVmss” z parametrem -InstanceView wyświetla stany OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="097f4-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-116">Az.IotHub</span></span>
* <span data-ttu-id="097f4-117">Nowe polecenia cmdlet do zarządzania konfiguracją bliźniaczej reprezentacji urządzenia IoT:</span><span class="sxs-lookup"><span data-stu-id="097f4-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="097f4-118">„Get-AzIotHubDeviceTwin”</span><span class="sxs-lookup"><span data-stu-id="097f4-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="097f4-119">„Update-AzIotHubDeviceTwin”</span><span class="sxs-lookup"><span data-stu-id="097f4-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="097f4-120">Dodano polecenie cmdlet do wywoływania metody bezpośredniej na urządzeniu w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="097f4-121">Nowe polecenia cmdlet do zarządzania konfiguracją bliźniaczej reprezentacji modułu urządzenia IoT:</span><span class="sxs-lookup"><span data-stu-id="097f4-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="097f4-122">„Get-AzIotHubModuleTwin”</span><span class="sxs-lookup"><span data-stu-id="097f4-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="097f4-123">„Update-AzIotHubModuleTwin”</span><span class="sxs-lookup"><span data-stu-id="097f4-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="097f4-124">Zarządzanie konfiguracją automatycznego zarządzania urządzeniami IoT na dużą skalę.</span><span class="sxs-lookup"><span data-stu-id="097f4-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="097f4-125">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-125">New cmdlets are:</span></span>
    - <span data-ttu-id="097f4-126">„Add-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="097f4-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="097f4-127">„Get-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="097f4-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="097f4-128">„Remove-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="097f4-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="097f4-129">„Set-AzIotHubConfiguration”</span><span class="sxs-lookup"><span data-stu-id="097f4-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="097f4-130">Dodano polecenie cmdlet do wywołania metody modułu brzegowego w centrum IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="097f4-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-131">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-132">Dodano nowe polecenie cmdlet „Update-AzKeyVault”, które umożliwia włączenie usuwania nietrwałego i ochrony przed oczyszczeniem w magazynie</span><span class="sxs-lookup"><span data-stu-id="097f4-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="097f4-133">Dodano obsługę do modułu Microsoft.PowerShell.SecretManagement [nr 11178]</span><span class="sxs-lookup"><span data-stu-id="097f4-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="097f4-134">Usunięto błąd w przykładach polecenia „Remove-AzKeyVaultManagedStorageSasDefinition” [nr 11479]</span><span class="sxs-lookup"><span data-stu-id="097f4-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="097f4-135">Dodano obsługę do prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="097f4-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="097f4-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="097f4-136">Az.Maintenance</span></span>
* <span data-ttu-id="097f4-137">Publikowanie ogólnie dostępnej wersji poleceń cmdlet modułu Maintenance</span><span class="sxs-lookup"><span data-stu-id="097f4-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-138">Az.Monitor</span></span>
* <span data-ttu-id="097f4-139">Dodano polecenia cmdlet dla zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="097f4-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="097f4-140">„Get-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="097f4-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="097f4-141">„Remove-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="097f4-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="097f4-142">„New-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="097f4-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="097f4-143">„Update-AzInsightsPrivateLinkScope”</span><span class="sxs-lookup"><span data-stu-id="097f4-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="097f4-144">„Get-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="097f4-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="097f4-145">„New-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="097f4-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="097f4-146">„Remove-AzInsightsPrivateLinkScopedResource”</span><span class="sxs-lookup"><span data-stu-id="097f4-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-147">Az.Network</span></span>
* <span data-ttu-id="097f4-148">Zaktualizowano polecenia cmdlet, aby umożliwić połączenie przy użyciu prywatnego adresu IP dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="097f4-149">„New-AzVirtualNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="097f4-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="097f4-150">„Set-AzVirtualNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="097f4-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="097f4-151">„New-AzVirtualNetworkGatewayConnection”</span><span class="sxs-lookup"><span data-stu-id="097f4-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="097f4-152">„Set-AzVirtualNetworkGatewayConnection”</span><span class="sxs-lookup"><span data-stu-id="097f4-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="097f4-153">Zaktualizowano polecenia cmdlet, aby umożliwić używanie elementów LocalNetworkGateways i VpnSites opartych na nazwach FQDN</span><span class="sxs-lookup"><span data-stu-id="097f4-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="097f4-154">„New-AzLocalNetworkGateway”</span><span class="sxs-lookup"><span data-stu-id="097f4-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="097f4-155">„New-AzVpnSiteLink”</span><span class="sxs-lookup"><span data-stu-id="097f4-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="097f4-156">Dodano obsługę rodziny adresów IPv6 w elemencie ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="097f4-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="097f4-157">Dodano polecenie „Set-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="097f4-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="097f4-158">Pozwala na ustawianie wszystkich istniejących właściwości, w tym IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="097f4-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="097f4-159">Zaktualizowano polecenie „Add-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="097f4-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="097f4-160">Dodano kolejny opcjonalny parametr AddressPrefixType umożliwiający określenie rodziny adresów prefiksu adresu</span><span class="sxs-lookup"><span data-stu-id="097f4-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="097f4-161">Zaktualizowano polecenia cmdlet, aby umożliwić ustawianie limitu czasu wykrywania nieaktywnych elementów równorzędnych w połączeniach bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="097f4-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="097f4-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-165">Dodano polecenie cmdlet „Start-AzPolicyComplianceScan” na potrzeby wyzwalania skanowania pod kątem zgodności z zasadami</span><span class="sxs-lookup"><span data-stu-id="097f4-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="097f4-166">Dodano definicję zasad, definicję zestawu i wersje przypisania do danych wyjściowych polecenia „Get-AzPolicyState”</span><span class="sxs-lookup"><span data-stu-id="097f4-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-168">Poprawiono formatowanie kodu i użyteczność przykładów polecenia „New-AzServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="097f4-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-169">Az.Sql</span></span>
* <span data-ttu-id="097f4-170">Dodano polecenia cmdlet „Get-AzSqlInstanceOperation” i „Stop-AzSqlInstanceOperation”</span><span class="sxs-lookup"><span data-stu-id="097f4-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="097f4-171">Dodano obsługę inspekcji do konta magazynu w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-172">Az.Storage</span></span>
* <span data-ttu-id="097f4-173">Dodano powiadomienie o zmianie powodującej niezgodność dotyczącej danych wyjściowych poleceń cmdlet dla plików platformy Azure, która zostanie wprowadzona w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="097f4-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="097f4-174">Dodano obsługę nowych wartości SkuName (StandardGZRS i StandardRAGZRS) podczas tworzenia/aktualizowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="097f4-175">„New-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="097f4-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="097f4-176">„Set-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="097f4-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="097f4-177">Dodano obsługę usługi Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="097f4-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="097f4-178">„New-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="097f4-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="097f4-179">„Get-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="097f4-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="097f4-180">„Get-AzDataLakeGen2ChildItem”</span><span class="sxs-lookup"><span data-stu-id="097f4-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="097f4-181">„Move-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="097f4-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="097f4-182">„Set-AzDataLakeGen2ItemAclObject”</span><span class="sxs-lookup"><span data-stu-id="097f4-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="097f4-183">„Update-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="097f4-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="097f4-184">„Get-AzDataLakeGen2ItemContent”</span><span class="sxs-lookup"><span data-stu-id="097f4-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="097f4-185">„Remove-AzDataLakeGen2Item”</span><span class="sxs-lookup"><span data-stu-id="097f4-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="097f4-186">Informacje o wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="097f4-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="097f4-187">3.7.0 — marzec 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-188">Az.Accounts</span></span>
* <span data-ttu-id="097f4-189">Rozwiązano problem powodujący zgłaszanie wyjątku NullReferenceException przez polecenia „Get-AzTenant”, „Get-AzDefault” i „Set-AzDefault”, gdy użytkownik nie jest zalogowany [nr 10292]</span><span class="sxs-lookup"><span data-stu-id="097f4-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-190">Az.Compute</span></span>
* <span data-ttu-id="097f4-191">Dodano następujące parametry do polecenia cmdlet „New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="097f4-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="097f4-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="097f4-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="097f4-193">Zezwolono na właściwość Encryption parametru Target polecenia cmdlet „New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="097f4-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="097f4-194">Rozwiązano problem tempDisk w przypadku poleceń cmdlet „Set-AzVmss” z parametrem -Reimage i „Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="097f4-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="097f4-195">[nr 11354]</span><span class="sxs-lookup"><span data-stu-id="097f4-195">[#11354]</span></span>
* <span data-ttu-id="097f4-196">Do poniższych poleceń cmdlet dodano obsługę nowego rozszerzenia SAP</span><span class="sxs-lookup"><span data-stu-id="097f4-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="097f4-197">„Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="097f4-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="097f4-198">„Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="097f4-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="097f4-199">„Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="097f4-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="097f4-200">„Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="097f4-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="097f4-201">Usunięto błędy w przykładach dokumentu pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="097f4-202">Pokazano dokładną wartość ciągu dla parametru PowerState maszyny wirtualnej w formacie tabeli.</span><span class="sxs-lookup"><span data-stu-id="097f4-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="097f4-203">„New-AzVmssConfig”: poprawiono serializację właściwości AutomaticRepairs, gdy właściwość SinglePlacementGroup jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="097f4-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="097f4-204">[nr 11257]</span><span class="sxs-lookup"><span data-stu-id="097f4-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-205">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-206">Zaktualizowano wersję zestawu ADF .Net SDK do 4.8.0</span><span class="sxs-lookup"><span data-stu-id="097f4-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="097f4-207">Dodano opcjonalne parametry do polecenia „Invoke-AzDataFactoryV2Pipeline” w celu obsługi ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="097f4-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-209">Dodano opis zmiany powodującej niezgodność dla poleceń „Export-AzDataLakeStoreItem” i „Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="097f4-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="097f4-210">Dodano opcję kodowania bajtów dla poleceń „New-AzDataLakeStoreItem”, „Add-AzDAtaLakeStoreItemContent” i „Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="097f4-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-211">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-212">Dodano obsługę określania minimalnej obsługiwanej wersji protokołu TLS podczas tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="097f4-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-213">Az.IotHub</span></span>
* <span data-ttu-id="097f4-214">Dodano obsługę zarządzania ustawieniami rozproszonymi dla poszczególnych urządzeń.</span><span class="sxs-lookup"><span data-stu-id="097f4-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="097f4-215">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="097f4-216">„Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="097f4-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="097f4-217">„Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="097f4-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-218">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-219">Dodano atrybuty zmian powodujących niezgodność do polecenia „New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="097f4-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-220">Az.Monitor</span></span>
* <span data-ttu-id="097f4-221">Zaktualizowano dokumentację polecenia „New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="097f4-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-222">Az.Network</span></span>
* <span data-ttu-id="097f4-223">Zaktualizowano polecenia cmdlet, aby zezwolić na połączenia VirtualHubVnetConnections między dzierżawami</span><span class="sxs-lookup"><span data-stu-id="097f4-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="097f4-224">„New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="097f4-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="097f4-225">„Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="097f4-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="097f4-226">„New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="097f4-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="097f4-227">„Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="097f4-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="097f4-228">Usunięto zależność od zestawu SDK zarządzania SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-230">Ulepszono komunikaty o błędach</span><span class="sxs-lookup"><span data-stu-id="097f4-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-232">W usłudze Azure Site Recovery dodano obsługę ponownego włączania ochrony oraz zaktualizowano właściwości maszyn wirtualnych w przypadku maszyn wirtualnych zaszyfrowanych za pomocą usługi Azure Disk Encryption.</span><span class="sxs-lookup"><span data-stu-id="097f4-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="097f4-233">Dodano monitorowanie odzyskiwania po awarii właściwości VmwareToAzure usługi Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="097f4-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="097f4-234">W usłudze Azure Backup dodano obsługę ponawiania aktualizacji zasad w przypadku elementów, dla których zakończyła się ona niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="097f4-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="097f4-235">W usłudze Azure Backup dodano obsługę ustawień wykluczania dysków podczas tworzenia i przywracania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="097f4-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="097f4-236">W usłudze Azure Backup dodano obsługę przywracania wielu plików/folderów w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="097f4-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="097f4-237">W usłudze Azure Backup dodano obsługę dla określonej przez użytkownika obsługi grupy zasobów w trakcie aktualizowania zasad IaasVM</span><span class="sxs-lookup"><span data-stu-id="097f4-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-238">Az.Resources</span></span>
* <span data-ttu-id="097f4-239">Poprawiono polecenie „Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType”, aby używało rzeczywistej wersji apiVersion zasobów, a nie domyślnej wersji apiVersion [nr 11267]</span><span class="sxs-lookup"><span data-stu-id="097f4-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="097f4-240">Dodano rejestrowanie identyfikatorów correlationId dla scenariuszy błędów</span><span class="sxs-lookup"><span data-stu-id="097f4-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="097f4-241">Niewielka zmiana dokumentacji polecenia „Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="097f4-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="097f4-242">Dodano przykład.</span><span class="sxs-lookup"><span data-stu-id="097f4-242">Added example.</span></span>
* <span data-ttu-id="097f4-243">Dodano znak ucieczki przed pojedynczym cudzysłowem w wartości parametru „Get-AzADUser” [nr 11317]</span><span class="sxs-lookup"><span data-stu-id="097f4-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="097f4-244">Dodano nowe polecenia cmdlet dla skryptów wdrażania („Get-AzDeploymentScript”, „Get-AzDeploymentScriptLog”, „Save-AzDeploymentScriptLog”, „Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="097f4-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-245">Az.Sql</span></span>
* <span data-ttu-id="097f4-246">Dodano możliwy do odczytu parametr pomocniczy do polecenia „Invoke-AzSqlDatabaseFailover”</span><span class="sxs-lookup"><span data-stu-id="097f4-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="097f4-247">Dodano polecenie cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication”</span><span class="sxs-lookup"><span data-stu-id="097f4-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="097f4-248">Zapisywanie stopnia czułości podczas klasyfikowania kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="097f4-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="097f4-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="097f4-249">Az.Support</span></span>
* <span data-ttu-id="097f4-250">Ogólna dostępność modułu „Az.Support”</span><span class="sxs-lookup"><span data-stu-id="097f4-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-251">Az.Websites</span></span>
* <span data-ttu-id="097f4-252">Dodano obsługę pracy z regułami routingu ruchu aplikacji internetowej za pośrednictwem poniższych nowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="097f4-253">„Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="097f4-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="097f4-254">„Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="097f4-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="097f4-255">„Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="097f4-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="097f4-256">„Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="097f4-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="097f4-257">3.6.1 — marzec 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-258">Az.Accounts</span></span>
* <span data-ttu-id="097f4-259">Otwarcie strony ankiety Azure PowerShell w poleceniu „Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="097f4-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="097f4-260">Wyświetlanie adresu URL ankiety Azure PowerShell w poleceniu „Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="097f4-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="097f4-261">Dodano wersję Az w agencie UserAgent</span><span class="sxs-lookup"><span data-stu-id="097f4-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-262">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-263">Dodano obsługę pobierania i konfigurowania domeny niestandardowej w punkcie końcowym DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="097f4-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="097f4-264">Dodano obsługę elementu „Export-AzApiManagementApi” do pobierania definicji interfejsu API w formacie JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="097f4-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="097f4-265">Dla polecenia „Import-AzApiManagementApi” dodano obsługę importowania definicji OpenApi 3.0 z dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="097f4-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="097f4-266">Dla poleceń „New-AzApiManagementIdentityProvider” i „Set-AzApiManagementIdentityProvider” dodano obsługę konfigurowania „dzierżawy podpisującej” dla dostawcy AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="097f4-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-268">Dodano odwołanie do elementu System.Buffers jawnie w plikach csproj i psd1.</span><span class="sxs-lookup"><span data-stu-id="097f4-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-269">Az.IotHub</span></span>
* <span data-ttu-id="097f4-270">Dodano obsługę zarządzania urządzeniami w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="097f4-271">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="097f4-272">„Add-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-273">„Get-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-274">„Remove-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-275">„Set-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="097f4-276">Dodano obsługę zarządzania modułami na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="097f4-277">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="097f4-278">„Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="097f4-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="097f4-279">„Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="097f4-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="097f4-280">„Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="097f4-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="097f4-281">„Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="097f4-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="097f4-282">Dodano polecenie cmdlet do pobierania parametrów połączenia docelowego urządzenia IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="097f4-283">Dodano polecenie cmdlet do pobierania parametrów połączenia modułu na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="097f4-284">Dodano obsługę pobierania/ustawiania urządzenia nadrzędnego urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="097f4-285">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="097f4-286">„Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="097f4-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="097f4-287">„Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="097f4-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="097f4-288">Dodano obsługę zarządzania relacją nadrzędny-podrzędny urządzenia.</span><span class="sxs-lookup"><span data-stu-id="097f4-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-289">Az.Monitor</span></span>
* <span data-ttu-id="097f4-290">Stała wartość wyjściowa polecenia „Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="097f4-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-291">Az.Network</span></span>
* <span data-ttu-id="097f4-292">Zaktualizowano zestaw SDK zarządzania SQL.</span><span class="sxs-lookup"><span data-stu-id="097f4-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="097f4-293">Rozwiązano problem z różnicą nazewnictwa w klasie PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="097f4-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="097f4-294">Mapowanie pola ActionsRequired na pole ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="097f4-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="097f4-295">Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="097f4-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-296">Az.Resources</span></span>
* <span data-ttu-id="097f4-297">Usunięto błąd odwołania o wartości null w elemencie „Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="097f4-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="097f4-298">Opcje „-Force” i „-PassThru” oznaczono jako opcjonalny w poleceniu „Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="097f4-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="097f4-299">Rozwiązano problem polegający na tym, że element „MailNickname” nie jest zwracany przez polecenie „Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="097f4-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="097f4-300">Rozwiązano problem polegający na tym, że operacja potoku „Remove-AzADGroup” nie działa [#11171]</span><span class="sxs-lookup"><span data-stu-id="097f4-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="097f4-301">Naprawiono błąd odwołania o wartości null w poleceniu GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="097f4-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="097f4-302">Dodano atrybuty zmiany powodującej niezgodność dla nadchodzących zmian w poleceniach cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="097f4-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="097f4-303">Zaktualizowano polecenie „Get-AzResourceGroup”, aby można było wykonać filtrowanie tagów grup zasobów po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="097f4-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="097f4-304">Rozszerzone polecenia cmdlet dotyczące tagów do akceptowania parametru -ResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="097f4-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="097f4-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="097f4-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="097f4-308">Dodano nowe polecenie cmdlet dotyczące tagów</span><span class="sxs-lookup"><span data-stu-id="097f4-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="097f4-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="097f4-310">Dodano element ScopedDeployment z zestawu SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="097f4-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-311">Az.Sql</span></span>
* <span data-ttu-id="097f4-312">Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="097f4-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="097f4-313">Dodano obsługę konfiguracji długoterminowego przechowywania kopii zapasowych dla zarządzanych baz danych</span><span class="sxs-lookup"><span data-stu-id="097f4-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="097f4-314">Pobieranie/ustawianie zasad LTR w zarządzanej bazie danych</span><span class="sxs-lookup"><span data-stu-id="097f4-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="097f4-315">Pobieranie kopii zapasowych LTR według zarządzanej bazy danych, wystąpienia zarządzanego lub lokalizacji</span><span class="sxs-lookup"><span data-stu-id="097f4-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="097f4-316">Usuwanie kopii zapasowej LTR</span><span class="sxs-lookup"><span data-stu-id="097f4-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="097f4-317">Przywracanie kopii zapasowej LTR, aby utworzyć nową zarządzaną bazę danych</span><span class="sxs-lookup"><span data-stu-id="097f4-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="097f4-318">Dodano parametr MinimalTlsVersion do polecenia New-AzSqlServer i Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="097f4-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="097f4-319">Dodano parametr MinimalTlsVersion do poleceń New-AzSqlInstance i Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="097f4-320">Niestandardowa wersja zestawu SQL SDK dla elementu Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-321">Az.Storage</span></span>
* <span data-ttu-id="097f4-322">Obsługiwane polecenie AllowProtectedAppendWrite w zasadach ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="097f4-323">„Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="097f4-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="097f4-324">Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu AzureStorageTable w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="097f4-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="097f4-325">„New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="097f4-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="097f4-326">„Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="097f4-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-327">Az.Websites</span></span>
* <span data-ttu-id="097f4-328">Dodano parametr tagu dla opcji „New-AzAppServicePlan” i „Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="097f4-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="097f4-329">Zatrzymaj wykonywanie polecenia cmdlet, jeśli podczas dodawania domeny niestandardowej do witryny internetowej zostanie zgłoszony wyjątek</span><span class="sxs-lookup"><span data-stu-id="097f4-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="097f4-330">Dodano obsługę wykonywania operacji dla usługi App Services nieznajdujących się w tej samej grupie zasobów co plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="097f4-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="097f4-331">Zastosowano ograniczenie dostępu do aplikacji internetowych/funkcji w różnych grupach zasobów</span><span class="sxs-lookup"><span data-stu-id="097f4-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="097f4-332">Rozwiązano problem w celu ustawienia niestandardowych nazw hostów dla miejsc aplikacji internetowych</span><span class="sxs-lookup"><span data-stu-id="097f4-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="097f4-333">3.5.0 — luty 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-334">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-334">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-335">Zaktualizowano telemetrię po stronie klienta.</span><span class="sxs-lookup"><span data-stu-id="097f4-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="097f4-336">W module Az.IotHub dodano polecenia cmdlet do obsługi zarządzania urządzeniami.</span><span class="sxs-lookup"><span data-stu-id="097f4-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="097f4-337">W module Az.SqlVirtualMachine dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="097f4-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-338">Az.Accounts</span></span>
* <span data-ttu-id="097f4-339">Dodano identyfikatory SubscriptionId i TenantId oraz czas wykonywania do danych telemetrii po stronie klienta</span><span class="sxs-lookup"><span data-stu-id="097f4-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-340">Az.Automation</span></span>
* <span data-ttu-id="097f4-341">Poprawiono literówkę w 1. przykładzie w dokumentacji referencyjnej polecenia „New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="097f4-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-343">Zaktualizowano zestaw SDK do wersji 7.0</span><span class="sxs-lookup"><span data-stu-id="097f4-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="097f4-344">Ulepszono komunikat o błędzie, gdy odpowiedź serwera ma pustą treść</span><span class="sxs-lookup"><span data-stu-id="097f4-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-345">Az.Compute</span></span>
* <span data-ttu-id="097f4-346">Dozwolono pustą wartość identyfikatora ProximityPlacementGroupId podczas aktualizacji</span><span class="sxs-lookup"><span data-stu-id="097f4-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-347">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-348">Dodano polecenie cmdlet służące do pobierania definicji reguł zarządzanych, które mogą być używane w zaporze aplikacji internetowej</span><span class="sxs-lookup"><span data-stu-id="097f4-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-349">Az.IotHub</span></span>
* <span data-ttu-id="097f4-350">Dodano obsługę zarządzania urządzeniami w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="097f4-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="097f4-351">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="097f4-352">„Add-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-353">„Get-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-354">„Remove-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="097f4-355">„Set-AzIotHubDevice”</span><span class="sxs-lookup"><span data-stu-id="097f4-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-356">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-357">Poprawiono zduplikowany tekst pliku Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="097f4-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-358">Az.Monitor</span></span>
* <span data-ttu-id="097f4-359">Poprawiono opis polecenia cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="097f4-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="097f4-360">Do polecenia „New-AzMetricAlertRuleV2” dodano nowy parametr o nazwie ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="097f4-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="097f4-361">Użytkownik może podać wartość ActionGroupId(ciąg) lub ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="097f4-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-362">Az.Network</span></span>
* <span data-ttu-id="097f4-363">Dodano jedną dodatkową uwagę dla parametru „-EnableProxyProtocol” polecenia cmdlet „New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="097f4-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="097f4-364">Poprawiono przykład opcji FilterData w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="097f4-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="097f4-365">Dodano przykład przechwytywania pakietów przedstawiający przechwytywanie wszystkich pakietów wewnętrznych i zewnętrznych w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="097f4-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="097f4-366">Obsługa zasad usługi Azure Firewall w przypadku zapór sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="097f4-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="097f4-367">Nie dodano żadnych nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-367">No new cmdlets are added.</span></span> <span data-ttu-id="097f4-368">Złagodzono ograniczenie dotyczące zasad zapór sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="097f4-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-370">Dodano obsługę funkcji przywracania jako plików dla baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="097f4-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-371">Az.Resources</span></span>
* <span data-ttu-id="097f4-372">Refaktoryzowano polecenia cmdlet wdrażania szablonów</span><span class="sxs-lookup"><span data-stu-id="097f4-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="097f4-373">Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w grupie zarządzania: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="097f4-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="097f4-374">Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w zakresie dzierżawy: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="097f4-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="097f4-375">Refaktoryzowano polecenia cmdlet \*-AzDeployment tak, aby działały konkretnie w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="097f4-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="097f4-376">Utworzono aliasy \*-AzSubscriptionDeployment dla poleceń cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="097f4-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="097f4-377">Poprawiono polecenie „Update-AzADApplication”, gdy parametr „AvailableToOtherTenants” nie jest ustawiony</span><span class="sxs-lookup"><span data-stu-id="097f4-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="097f4-378">Usunięto zestaw parametrów ApplicationObjectWithoutCredentialParameterSet, aby uniknąć wyjątku AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="097f4-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="097f4-379">Ponownie wygenerowano pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-380">Az.Sql</span></span>
* <span data-ttu-id="097f4-381">Dodano obsługę przywracania do punktu w czasie w wystąpieniach zarządzanych między subskrypcjami.</span><span class="sxs-lookup"><span data-stu-id="097f4-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="097f4-382">Dodano obsługę zmiany obecnej generacji sprzętu wystąpienia zarządzanego SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="097f4-383">Poprawiono przykłady w pomocy polecenia „Update-AzSqlServerVulnerabilityAssessmentSetting”: dane wyjściowe parametru/właściwości — EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="097f4-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="097f4-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="097f4-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="097f4-385">Dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="097f4-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="097f4-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="097f4-386">Az.StorageSync</span></span>
* <span data-ttu-id="097f4-387">Zaktualizowano obsługiwane zestawy znaków w poleceniu „Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="097f4-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="097f4-388">3.4.0 — luty 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-389">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-389">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-390">Wydano początkową wersję 0.1.0 funkcji Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="097f4-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="097f4-391">Dodano obsługę funkcji Az.Network ConnectionMonitor w wersji 2</span><span class="sxs-lookup"><span data-stu-id="097f4-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-392">Az.Accounts</span></span>
* <span data-ttu-id="097f4-393">Wyłączono automatyczne zapisywanie kontekstu, gdy plik AzureRmContext.json jest niedostępny</span><span class="sxs-lookup"><span data-stu-id="097f4-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="097f4-394">Zaktualizowano odwołania do programu Azure PowerShell Common do wersji 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="097f4-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-395">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-396">**Get-AzApiManagementApiSchema** Naprawiono pobieranie schematu Open-Api skojarzonego z interfejsem API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="097f4-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="097f4-397">**New-AzApiManagementProduct**\* i **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="097f4-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="097f4-398">Poprawiono dokumentację dotycząca funkcji https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="097f4-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="097f4-399">**Set-AzApiManagementApi** Dodano przykład pokazujący, jak zaktualizować wartość ServiceUrl przy użyciu polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-400">Az.Compute</span></span>
* <span data-ttu-id="097f4-401">Ograniczono liczbę stanów maszyn wirtualnych do 100, aby uniknąć ograniczania w przypadku wykonywania operacji Get-AzVM -Status bez nazwy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="097f4-402">Dodano polecenie cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="097f4-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="097f4-403">Dodano parametry EncryptionType i DiskEncryptionSetId do następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="097f4-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="097f4-405">Dodano parametr ColocationStatus do polecenia cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="097f4-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-406">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-407">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.7.0</span><span class="sxs-lookup"><span data-stu-id="097f4-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="097f4-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="097f4-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="097f4-409">Dodano operacje LIST dla zasobów</span><span class="sxs-lookup"><span data-stu-id="097f4-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="097f4-410">Dodano możliwość wykonywania operacji na krokach kontroli kondycji</span><span class="sxs-lookup"><span data-stu-id="097f4-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-411">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-412">Naprawiono błąd w dokumentacji funkcji New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="097f4-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-413">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-414">Dodano alias Name do atrybutu VaultName, aby uspójnić polecenie Remove-AzureKeyVault z poleceniem New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="097f4-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-415">Az.Network</span></span>
* <span data-ttu-id="097f4-416">Dodano nowy przykład do polecenia Set-AzNetworkWatcherConfigFlowLog.md w celu zademonstrowania scenariusza wyłączenia analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="097f4-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="097f4-417">Dodano obsługę przypisywania konfiguracji protokołu IP zarządzania do zapory Azure Firewall — dedykowanej podsieci i publicznego adresu IP, których zapora będzie używać dla swojego ruchu związanego z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="097f4-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="097f4-418">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="097f4-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="097f4-419">Dodano parametr -ManagementPublicIpAddress (nieobowiązkowy), który akceptuje obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="097f4-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="097f4-420">Dodano metodę SetManagementIpConfiguration w obiekcie zapory — wymaga jako danych wejściowych podsieci i publicznego adresu IP — nazwa podsieci musi mieć wartość „AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="097f4-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="097f4-421">Poprawiono przykłady polecenia Get-AzNetworkSecurityGroup, aby pokazać przykłady dla sieciowej grupy zabezpieczeń zamiast interfejsów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="097f4-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="097f4-422">Poprawiono literówkę w poleceniu New-AzVpnSite, która uniemożliwiała modułowi wypełniania identyfikatora wypełnienie parametru.</span><span class="sxs-lookup"><span data-stu-id="097f4-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="097f4-423">Dodano obsługę konfiguracji adresu URL w akcji reguł ponownego zapisywania ustawionej w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="097f4-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="097f4-424">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-424">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="097f4-426">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="097f4-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="097f4-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="097f4-428">Dodano obsługę dla zasobów NetworkWatcher ConnectionMonitor w wersji 2</span><span class="sxs-lookup"><span data-stu-id="097f4-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-430">Obsługa oceny zgodności przed ustaleniem, który zasób należy skorygować</span><span class="sxs-lookup"><span data-stu-id="097f4-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="097f4-431">Dodano parametr „-ResourceDiscoverMode” do polecenia Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="097f4-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="097f4-432">Dodano polecenie cmdlet Get-AzPolicyMetadata na potrzeby pobierania zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="097f4-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="097f4-433">Zaktualizowano polecenia Get-AzPolicyState i Get-AzPolicyStateSummary dla interfejsu API w wersji 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="097f4-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-435">Usługa Azure Site Recovery obsługuje usuwanie zreplikowanego dysku.</span><span class="sxs-lookup"><span data-stu-id="097f4-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="097f4-436">W usłudze Azure Backup dodano obsługę dodawania tagów podczas tworzenia magazynu usługi Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="097f4-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-437">Az.Resources</span></span>
* <span data-ttu-id="097f4-438">Parametr -Scope ustawiono jako opcjonalny w poleceniach cmdlet \*-AzPolicyAssignment z domyślną wartością subskrypcji kontekstu</span><span class="sxs-lookup"><span data-stu-id="097f4-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="097f4-439">Dodano przykłady tworzenia obiektu ADServicePrincipal z hasłem i kluczowym poświadczeniem</span><span class="sxs-lookup"><span data-stu-id="097f4-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-440">Az.Sql</span></span>
<span data-ttu-id="097f4-441">Naprawiono polecenie cmdlet New-AzSqlDatabaseSecondary, aby sprawdzało istnienie elementu PartnerDatabaseName zamiast istnienia elementu DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="097f4-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-442">Az.Storage</span></span>
* <span data-ttu-id="097f4-443">Włączono obsługę typu klucza szyfrowania tabeli/kolejki w tworzeniu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="097f4-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="097f4-445">Pokazywana jest wartość RequestId, gdy właściwość StorageException nie ma wartości ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="097f4-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="097f4-446">Poprawiono przykład 6 polecenia cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-447">Az.Websites</span></span>
* <span data-ttu-id="097f4-448">Polecenia Set-AzWebapp i Set-AzWebappSlot obsługują właściwości AlwaysOn, MinTls i FtpsState</span><span class="sxs-lookup"><span data-stu-id="097f4-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="097f4-449">Rozwiązywanie problemu polegającego na tym, że zmienianie ustawienia HttpsOnly jednocześnie ze zmienianiem ustawienia AppservicePlan za pomocą jednego polecenia Set-AzWebApp powodowało resetowanie ustawienia HttpsOnly do wartości domyślnej</span><span class="sxs-lookup"><span data-stu-id="097f4-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="097f4-450">3.3.0 — styczeń 2020 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-451">Az.Accounts</span></span>
* <span data-ttu-id="097f4-452">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametry AzureAttestationServiceEndpointResourceId i AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="097f4-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-453">Az.Cdn</span></span>
* <span data-ttu-id="097f4-454">Wyświetlanie szczegółów odpowiedzi błędu w poleceniu cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-455">Az.Compute</span></span>
* <span data-ttu-id="097f4-456">Poprawiono polecenie cmdlet Set-AzVMCustomScriptExtension dla maszyny wirtualnej z zarządzanym dyskiem systemu operacyjnego, który nie ma profilu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="097f4-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="097f4-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="097f4-458">Naprawiono nazwy parametrów używanych na przykład przez polecenie New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="097f4-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="097f4-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="097f4-460">Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="097f4-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="097f4-461">Pobieranie kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="097f4-462">Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="097f4-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="097f4-463">Tworzenie nowego kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="097f4-464">Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="097f4-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="097f4-465">Usuwanie kontenera magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="097f4-466">Dodano polecenie cmdlet „Invoke-AzDataBoxEdgeStorageContainer”</span><span class="sxs-lookup"><span data-stu-id="097f4-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="097f4-467">Wywoływanie akcji odświeżania danych w kontenerze magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="097f4-468">Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="097f4-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="097f4-469">Pobieranie konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="097f4-470">Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="097f4-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="097f4-471">Tworzenie nowego konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="097f4-472">Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="097f4-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="097f4-473">Usuwanie konta magazynu usługi Edge</span><span class="sxs-lookup"><span data-stu-id="097f4-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="097f4-474">Wywołanie polecenia cmdlet „Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="097f4-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="097f4-475">Wywołanie akcji odświeżania danych w udziale</span><span class="sxs-lookup"><span data-stu-id="097f4-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="097f4-476">Dodano polecenie cmdlet „Set-AzDataBoxEdgeStorageAccountCredential”</span><span class="sxs-lookup"><span data-stu-id="097f4-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="097f4-477">Ustawienie poświadczenia konta magazynu az databoxedge</span><span class="sxs-lookup"><span data-stu-id="097f4-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-478">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-479">Dodano właściwości AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId i VersionStatus do polecenia Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="097f4-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="097f4-480">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.6.0</span><span class="sxs-lookup"><span data-stu-id="097f4-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="097f4-481">Dodano parametr „PublicIPs” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu umożliwienia tworzenia środowisk IR Azure-SSIS ze statycznymi publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="097f4-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="097f4-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="097f4-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="097f4-483">Usunięto niedziałający link w pliku Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="097f4-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-484">Az.EventHub</span></span>
* <span data-ttu-id="097f4-485">Rozwiązano problem nr 10634: Naprawiono odwołanie do obiektu null podczas usuwania elementu eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="097f4-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-486">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-487">Poprawiono błąd w pliku Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="097f4-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="097f4-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="097f4-488">Az.MachineLearning</span></span>
* <span data-ttu-id="097f4-489">Usunięto poniższe polecenia cmdlet, ponieważ funkcja MachineLearningCompute nie jest już dostępna</span><span class="sxs-lookup"><span data-stu-id="097f4-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="097f4-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="097f4-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="097f4-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="097f4-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="097f4-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="097f4-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="097f4-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="097f4-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="097f4-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="097f4-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="097f4-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="097f4-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="097f4-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="097f4-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-497">Az.Network</span></span>
* <span data-ttu-id="097f4-498">Uaktualniono zależność Microsoft.Azure.Management.Sql z wersji 1.36-preview do 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="097f4-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-500">W usłudze Azure Site Recovery zmieniono obsługę maszyn wirtualnych z dyskiem zarządzanym szyfrowanych podczas magazynowania za pomocą kluczy zarządzanych przez klienta dla platformy Azure na dostawcę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="097f4-501">Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego podczas włączania ochrony dla narzędzia VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="097f4-502">Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego na poziomie dysku w celu włączenia ochrony dla narzędzia VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="097f4-503">Usługa Azure Site Recovery obsługuje aktualizację elementu chronionego przez replikację z zestawem szyfrowania dysków mapowanym dla funkcji HyperV na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-504">Az.Resources</span></span>
* <span data-ttu-id="097f4-505">Naprawiono błąd w dokumencie pomocy „Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="097f4-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-506">Az.Sql</span></span>
* <span data-ttu-id="097f4-507">Naprawiono błąd oceny luk w zabezpieczeniach dotyczący funkcji poleceń cmdlet do ustawiania punktu odniesienia w celu działania na bazie danych master dla usługi Azure Database i ograniczenia go w systemowych bazach danych wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="097f4-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="097f4-508">Naprawiono błąd podczas tworzenia grupy trybu failover wystąpienia SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="097f4-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="097f4-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="097f4-510">Dodano nowy prawidłowy typ licencji DR</span><span class="sxs-lookup"><span data-stu-id="097f4-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-511">Az.Storage</span></span>
* <span data-ttu-id="097f4-512">Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu DefaultAction w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="097f4-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="097f4-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="097f4-514">Obsługa uzyskiwania ostatniego czasu synchronizacji kont usługi Storage poprzez uruchomienie polecenia get-AzureRMStorageAccount z parametrem -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="097f4-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="097f4-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="097f4-516">3.2.0 — grudzień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="097f4-517">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-517">General</span></span>
* <span data-ttu-id="097f4-518">Zaktualizowano odwołania w pliku psd1 tak, aby dla wszystkich modułów były używane ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="097f4-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-519">Az.Accounts</span></span>
* <span data-ttu-id="097f4-520">Ustawiono prawidłowego agenta użytkownika dla telemetrii po stronie klienta dla modułu Az 4.0 (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="097f4-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="097f4-521">Wyświetlanie przyjaznego dla użytkownika komunikatu o błędzie, gdy kontekst ma wartość null, w module Az 4.0 (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="097f4-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="097f4-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-522">Az.Batch</span></span>
* <span data-ttu-id="097f4-523">Rozwiązano problem [nr 10602](https://github.com/Azure/azure-powershell/issues/10602) uniemożliwiający poleceniu **New-AzBatchPool** prawidłowe wysyłanie elementów „VirtualMachineConfiguration.ContainerConfiguration” i „VirtualMachineConfiguration.DataDisks” do serwera.</span><span class="sxs-lookup"><span data-stu-id="097f4-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-524">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-525">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.5.0</span><span class="sxs-lookup"><span data-stu-id="097f4-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-526">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-527">Dodano obsługę wykluczania reguł zarządzanych przez zaporę aplikacji internetowej</span><span class="sxs-lookup"><span data-stu-id="097f4-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="097f4-528">Dodano element SocketAddr do autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="097f4-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="097f4-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="097f4-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="097f4-530">Obsługa wyjątków</span><span class="sxs-lookup"><span data-stu-id="097f4-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-531">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-532">Usunięto błąd podczas uzyskiwania dostępu do wartości, która potencjalnie nie jest ustawiona</span><span class="sxs-lookup"><span data-stu-id="097f4-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="097f4-533">Zarządzanie certyfikatami kryptografii opartej na krzywej eliptycznej</span><span class="sxs-lookup"><span data-stu-id="097f4-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="097f4-534">Dodano obsługę określania krzywej dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="097f4-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-535">Az.Monitor</span></span>
* <span data-ttu-id="097f4-536">Dodanie opcjonalnego argumentu do polecenia dodania ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="097f4-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="097f4-537">Argument przełącznika, który, jeśli zostanie podany, wskazuje, że eksportowanie do usługi Log Analytics musi być przeprowadzane do ustalonego schematu (tzn.</span><span class="sxs-lookup"><span data-stu-id="097f4-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="097f4-538">typu danych, dedykowanego)</span><span class="sxs-lookup"><span data-stu-id="097f4-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-539">Az.Network</span></span>
* <span data-ttu-id="097f4-540">Obsługa grup adresów IP w regułach sieci, translatorze adresów sieciowych i aplikacji usługi Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="097f4-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-541">Az.Resources</span></span>
* <span data-ttu-id="097f4-542">Usunięto problem polegający na tym, że wdrożenie szablonu nie może odczytać parametru szablonu, jeśli jego nazwa powoduje konflikt z nazwą wbudowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="097f4-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="097f4-543">Zaktualizowano polecenia cmdlet zasad w celu używania nowej wersji interfejsu API 2019-09-01, która wprowadza obsługę grupowania w definicjach zestawów zasad.</span><span class="sxs-lookup"><span data-stu-id="097f4-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-544">Az.Sql</span></span>
* <span data-ttu-id="097f4-545">Uaktualniono tworzenie magazynu w automatycznym włączaniu oceny luk w zabezpieczeniach do wersji StorageV2</span><span class="sxs-lookup"><span data-stu-id="097f4-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-546">Az.Storage</span></span>
* <span data-ttu-id="097f4-547">Obsługa generowania tokenów SAS opartych na tożsamości kontenera / obiektu blob z kontekstem magazynu w oparciu o uwierzytelnianie OAuth</span><span class="sxs-lookup"><span data-stu-id="097f4-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="097f4-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="097f4-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="097f4-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="097f4-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="097f4-550">Obsługa odwoływania kluczy delegowania użytkowników dla konta magazynu w celu odwołania wszystkich tokenów SAS tożsamości</span><span class="sxs-lookup"><span data-stu-id="097f4-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="097f4-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="097f4-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="097f4-552">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 14.2.0 w celu obsługi nowego interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="097f4-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="097f4-553">Obsługa funkcji QuotaGiB (udostępnianie limitu przydziału w GiB) dla wartości powyżej 5120 w poleceniach cmdlet płaszczyzny zarządzania udziałem plików i dodano alias parametru „Quota” do parametru „QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="097f4-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="097f4-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="097f4-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="097f4-556">Dodano alias parametru „QuotaGiB” do parametru „Quota”</span><span class="sxs-lookup"><span data-stu-id="097f4-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="097f4-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="097f4-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="097f4-558">Rozwiązano problem z czyszczeniem zapisanych zasad dostępu przez polecenie Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="097f4-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="097f4-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="097f4-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="097f4-560">3.1.0 — listopad 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-561">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-561">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-562">Wydano pakiet Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="097f4-563">Wydano pakiet Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-564">Az.Compute</span></span>
* <span data-ttu-id="097f4-565">Funkcja ponownego stosowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-565">VM Reapply feature</span></span>
    - <span data-ttu-id="097f4-566">Dodano parametr Reapply do polecenia cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="097f4-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="097f4-567">Funkcja AutomaticRepairs zestawu skalowania maszyn wirtualnych:</span><span class="sxs-lookup"><span data-stu-id="097f4-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="097f4-568">Dodano parametry EnableAutomaticRepair, AutomaticRepairGracePeriod i AutomaticRepairMaxInstanceRepairsPercent do następujących poleceń cmdlet:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="097f4-569">Obsługa obrazów z galerii pomiędzy dzierżawami dla polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="097f4-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="097f4-570">Dodano element „Spot” do modułu wypełniania argumentów parametru Priority w poleceniach cmdlet New-AzVM, New-AzVMConfig i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="097f4-571">Dodano parametry DiskIOPSReadWrite i DiskMBpsReadWrite do polecenia cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="097f4-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="097f4-572">Zmieniono parametr SourceImageId polecenia cmdlet New-AzGalleryImageVersion na opcjonalny</span><span class="sxs-lookup"><span data-stu-id="097f4-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="097f4-573">Dodano parametry OSDiskImage i DataDiskImage do polecenia cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="097f4-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="097f4-574">Dodano parametr HyperVGeneration do polecenia cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="097f4-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="097f4-575">Dodano parametry SkipExtensionsOnOverprovisionedVMs do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="097f4-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="097f4-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="097f4-577">Dodano polecenie cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="097f4-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="097f4-578">Pobieranie zamówienia</span><span class="sxs-lookup"><span data-stu-id="097f4-578">Get the Order</span></span>
* <span data-ttu-id="097f4-579">Dodano polecenie cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="097f4-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="097f4-580">Utworzono nowe zamówienie</span><span class="sxs-lookup"><span data-stu-id="097f4-580">Create new Order</span></span>
* <span data-ttu-id="097f4-581">Dodano polecenie cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="097f4-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="097f4-582">Usunięto zamówienie</span><span class="sxs-lookup"><span data-stu-id="097f4-582">Remove the Order</span></span>
* <span data-ttu-id="097f4-583">Zmiana w poleceniu cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="097f4-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="097f4-584">Teraz tworzy lokalny udział plików</span><span class="sxs-lookup"><span data-stu-id="097f4-584">Now creates Local Share</span></span>
* <span data-ttu-id="097f4-585">Dodano polecenie cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="097f4-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="097f4-586">Teraz można zamapować wartość IotRole na udział plików</span><span class="sxs-lookup"><span data-stu-id="097f4-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="097f4-587">Dodano polecenie cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="097f4-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="097f4-588">Wywoływanie skanowania aktualizacji, pobierania aktualizacji, instalowania aktualizacji na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="097f4-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="097f4-589">Dodano polecenie cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="097f4-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="097f4-590">Pobiera informacje o wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="097f4-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="097f4-591">Dodano polecenie cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="097f4-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="097f4-592">Utworzono nowe wyzwalacze</span><span class="sxs-lookup"><span data-stu-id="097f4-592">Create new Triggers</span></span>
* <span data-ttu-id="097f4-593">Dodano polecenie cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="097f4-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="097f4-594">Usunięto wyzwalacze</span><span class="sxs-lookup"><span data-stu-id="097f4-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-595">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-596">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.4.0</span><span class="sxs-lookup"><span data-stu-id="097f4-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="097f4-597">Dodano parametr „ExpressCustomSetup” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu włączenia konfiguracji i składników innych firm bez niestandardowego skryptu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="097f4-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-599">Zaktualizowano dokumentację poleceń Get-AzDataLakeStoreDeletedItem i Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="097f4-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-600">Az.EventHub</span></span>
* <span data-ttu-id="097f4-601">Rozwiązano problem nr 10301: Poprawiono format daty tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="097f4-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-602">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-603">Dodano parametr MinimumTlsVersion do poleceń Enable-AzFrontDoorCustomDomainHttps i New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="097f4-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="097f4-604">Dodano parametry HealthProbeMethod i EnabledState do polecenia New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="097f4-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="097f4-605">Dodano nowe polecenie cmdlet do tworzenia obiektu BackendPoolsSettings w celu przejścia do tworzenia/aktualizacji usługi Front Door</span><span class="sxs-lookup"><span data-stu-id="097f4-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="097f4-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="097f4-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-607">Az.Network</span></span>
* <span data-ttu-id="097f4-608">Zmieniono przykłady opcji FilterData dla plików „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md” i „Start-AzVirtualnetworkGatewayPacketCapture.md”.</span><span class="sxs-lookup"><span data-stu-id="097f4-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="097f4-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="097f4-609">Az.PrivateDns</span></span>
* <span data-ttu-id="097f4-610">Zaktualizowano zestaw .Net SDK usługi PrivateDns do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-612">Obsługa usługi Azure Site Recovery w celu wybrania typu dysku przy włączaniu ochrony.</span><span class="sxs-lookup"><span data-stu-id="097f4-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="097f4-613">Poprawka edycji akcji planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="097f4-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="097f4-614">Obsługa przywracania SQL usługi Azure Backup w celu akceptowania baz danych strumienia pliku.</span><span class="sxs-lookup"><span data-stu-id="097f4-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="097f4-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="097f4-615">Az.RedisCache</span></span>
* <span data-ttu-id="097f4-616">Dodano parametr „MinimumTlsVersion” w poleceniach cmdlet „New-AzRedisCache” i „Set-AzRedisCache”.</span><span class="sxs-lookup"><span data-stu-id="097f4-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="097f4-617">Ponadto dodano parametr „MinimumTlsVersion” do danych wyjściowych polecenia cmdlet „Get-AzRedisCache”.</span><span class="sxs-lookup"><span data-stu-id="097f4-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="097f4-618">Dodano weryfikację parametru „-Size” dla poleceń cmdlet „Set-AzRedisCache” i „New-AzRedisCache”</span><span class="sxs-lookup"><span data-stu-id="097f4-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-619">Az.Resources</span></span>
- <span data-ttu-id="097f4-620">Zaktualizowano polecenia cmdlet zasad, aby używały nowego interfejsu API w wersji 2019-06-01, który ma nową właściwość EnforcementMode w przypisaniu zasad.</span><span class="sxs-lookup"><span data-stu-id="097f4-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="097f4-621">Zaktualizowano przykład pomocy definicji zasad tworzenia</span><span class="sxs-lookup"><span data-stu-id="097f4-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="097f4-622">Usunięto usterkę polegającą na tym, że polecenie Remove-AZADServicePrincipal -ServicePrincipalName zwracało pustą referencję, gdy nie znajdowano głównej nazwy usługi.</span><span class="sxs-lookup"><span data-stu-id="097f4-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="097f4-623">Usunięto usterkę polegającą na tym, że polecenie New-AZADServicePrincipal zwracało pustą referencję, gdy dzierżawa nie miała żadnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="097f4-624">Zmieniono polecenie New-AzAdServicePrincipal w celu dodania poświadczeń tylko do skojarzonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="097f4-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-625">Az.Sql</span></span>
* <span data-ttu-id="097f4-626">Dodano obsługę bazy danych ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="097f4-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="097f4-627">Naprawiono polecenie Set-AzSqlDatabase w przypadku, gdy nie ustawiono nadmiarowości strefy</span><span class="sxs-lookup"><span data-stu-id="097f4-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="097f4-628">3.0.0 — listopad 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="097f4-629">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-629">General</span></span>
* <span data-ttu-id="097f4-630">Wydano pakiet Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-631">Az.Accounts</span></span>
* <span data-ttu-id="097f4-632">Dodano komunikat o zakończeniu obsługi aliasu „Resolve-Error”.</span><span class="sxs-lookup"><span data-stu-id="097f4-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="097f4-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="097f4-633">Az.Advisor</span></span>
* <span data-ttu-id="097f4-634">Dodano nową kategorię „Operational Excellence” do polecenia cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="097f4-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="097f4-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-635">Az.Batch</span></span>
* <span data-ttu-id="097f4-636">Nazwę elementu `CoreQuota` dla klasy `BatchAccountContext` zmieniono na `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="097f4-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="097f4-637">Jest również nowa właściwość `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="097f4-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="097f4-638">Ma to wpływ na polecenie **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="097f4-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="097f4-639">Parametr polecenia cmdlet **New-AzBatchTask** `-ResourceFile` teraz przyjmuje kolekcję obiektów `PSResourceFile`, którą można utworzyć przy użyciu nowego polecenia cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="097f4-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="097f4-640">Nowe polecenie cmdlet **New-AzBatchResourceFile** w celu ułatwienia tworzenia obiektów `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="097f4-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="097f4-641">Można je dostarczyć do polecenia cmdlet **New-AzBatchTask** w parametrze `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="097f4-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="097f4-642">Obsługuje ono dwa nowe rodzaje plików zasobów oprócz istniejącego sposobu `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="097f4-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="097f4-643">Pliki zasobów oparte na elemencie `AutoStorageContainerName` pobierają cały kontener automatycznego magazynu do węzła usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="097f4-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="097f4-644">Pliki zasobów oparte na elemencie `StorageContainerUrl` pobierają kontener określony w adresie URL do węzła usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="097f4-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="097f4-645">Usunięto właściwość `ApplicationPackages` elementu `PSApplication` zwracaną przez polecenie cmdlet **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="097f4-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="097f4-646">Określone pakiety wewnątrz aplikacji można teraz pobrać przy użyciu polecenia cmdlet **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="097f4-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="097f4-647">Na przykład: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="097f4-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="097f4-648">Zmieniono nazwę właściwości `ApplicationId` na `ApplicationName` w poleceniach cmdlet **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** i **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="097f4-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="097f4-649">`ApplicationId` teraz jest aliasem `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="097f4-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="097f4-650">Dodano nową właściwość `PSWindowsUserConfiguration` do klasy `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="097f4-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="097f4-651">Zmieniono nazwę właściwości `Version` na `Name` w klasie `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="097f4-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="097f4-652">Zmieniono nazwę właściwości `BlobSource` na `HttpUrl` w klasie `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="097f4-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="097f4-653">Usunięto właściwość `OSDisk` z klasy `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="097f4-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="097f4-654">Usunięto polecenie cmdlet **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="097f4-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="097f4-655">Ta operacja nie jest już obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="097f4-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="097f4-656">Usunięto właściwość `TargetOSVersion` z klasy `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="097f4-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="097f4-657">Zmieniono nazwę właściwości `CurrentOSVersion` na `OSVersion` w klasie `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="097f4-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="097f4-658">Usunięto właściwości `DataEgressGiB` i `DataIngressGiB` z klasy `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="097f4-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="097f4-659">Usunięto polecenie cmdlet **Get-AzBatchNodeAgentSku** i zastąpiono je poleceniem cmdlet **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="097f4-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="097f4-660">Polecenie cmdlet **Get-AzBatchSupportedImage** zwraca te same dane co polecenie cmdlet **Get-AzBatchNodeAgentSku**, ale w bardziej przyjaznym formacie.</span><span class="sxs-lookup"><span data-stu-id="097f4-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="097f4-661">Teraz są również zwracane nowe obrazy niezweryfikowane.</span><span class="sxs-lookup"><span data-stu-id="097f4-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="097f4-662">Uwzględniono również dodatkowe informacje na temat właściwości `Capabilities` i `BatchSupportEndOfLife` dla każdego obrazu.</span><span class="sxs-lookup"><span data-stu-id="097f4-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="097f4-663">Dodano możliwość instalowania zdalnych systemów plików na każdym węźle puli za pośrednictwem nowego parametru `MountConfiguration` polecenia cmdlet **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="097f4-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="097f4-664">Teraz obsługiwane są reguły zabezpieczeń sieciowych blokujące dostęp sieciowy do puli na podstawie portu źródłowego ruchu.</span><span class="sxs-lookup"><span data-stu-id="097f4-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="097f4-665">Jest to realizowane za pomocą właściwości `SourcePortRanges` w klasie `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="097f4-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="097f4-666">Podczas uruchamiania kontenera usługa Batch obsługuje teraz wykonywanie zadania w katalogu roboczym kontenera lub w katalogu roboczym zadania usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="097f4-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="097f4-667">Jest to kontrolowane przez właściwość `WorkingDirectory` w klasie `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="097f4-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="097f4-668">Dodano możliwość określania kolekcji publicznych adresów IP w klasie `PSNetworkConfiguration` za pośrednictwem nowej właściwości `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="097f4-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="097f4-669">To gwarantuje, że węzły w puli będą miały adres IP z listy adresów IP dostarczonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="097f4-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="097f4-670">Gdy nie zostanie określona, wartością domyślną opcji `WaitForSuccess` w klasie `PSSTartTask` jest teraz `$True` (była wartość `$False`).</span><span class="sxs-lookup"><span data-stu-id="097f4-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="097f4-671">Gdy nie zostanie określona, wartością domyślną opcji `Scope` w klasie `PSAutoUserSpecification` jest teraz `Pool` (była wartość `Task` w systemie Windows i `Pool` w systemie Linux).</span><span class="sxs-lookup"><span data-stu-id="097f4-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-672">Az.Cdn</span></span>
* <span data-ttu-id="097f4-673">Wprowadzono akcje UrlRewriteAction i CacheKeyQueryStringAction do aparatu RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="097f4-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="097f4-674">Usunięto kilka usterek, takich jak brakujące dane wejściowe „Selector” w poleceniu cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="097f4-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-675">Az.Compute</span></span>
* <span data-ttu-id="097f4-676">Funkcja zestawu szyfrowania dysków</span><span class="sxs-lookup"><span data-stu-id="097f4-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="097f4-677">Nowe polecenia cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="097f4-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="097f4-678">Dodano parametr DiskEncryptionSetId do następujących poleceń cmdlet:   Set-AzImageOSDisk, Set-AzVMOSDisk, Set-AzVmssStorageProfile, Add-AzImageDataDisk, New-AzVMDataDisk, Set-AzVMDataDisk, Add-AzVMDataDisk, Add-AzVmssDataDisk i Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="097f4-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="097f4-679">Dodano parametry DiskEncryptionSetId i EncryptionType do następujących poleceń cmdlet:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="097f4-680">Dodano parametr Add PublicIPAddressVersion do polecenia cmdlet New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="097f4-681">Właściwość FileUris rozszerzenia niestandardowego skryptu przeniesiono z ustawienia publicznego do ustawienia chronionego</span><span class="sxs-lookup"><span data-stu-id="097f4-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="097f4-682">Dodano parametr ScaleInPolicy do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="097f4-683">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="097f4-683">Breaking changes</span></span>
    - <span data-ttu-id="097f4-684">Parametr UploadSizeInBytes jest używany zamiast parametru DiskSizeGB dla polecenia cmdlet New-AzDiskConfig, gdy opcja CreateOption ma wartość Upload</span><span class="sxs-lookup"><span data-stu-id="097f4-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="097f4-685">Element PublishingProfile.Source.ManagedImage.Id został zastąpiony elementem StorageProfile.Source.Id w obiekcie GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="097f4-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-686">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-687">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.3.0</span><span class="sxs-lookup"><span data-stu-id="097f4-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-689">Aktualizacja wersji zestawu SDK ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), wprowadza następujące poprawki</span><span class="sxs-lookup"><span data-stu-id="097f4-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="097f4-690">Unikanie zgłaszania wyjątku, gdy nie można zdeserializować elementu creationtime wpisu kosza lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="097f4-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="097f4-691">Uwidacznianie ustawienia dla limitu czasu żądania w obiekcie adlsclient</span><span class="sxs-lookup"><span data-stu-id="097f4-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="097f4-692">Naprawiono przekazywanie oryginalnej flagi syncflag na potrzeby odzyskiwania badoffset</span><span class="sxs-lookup"><span data-stu-id="097f4-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="097f4-693">Naprawiono klasę EnumerateDirectory, aby pobierała token kontynuacji po sprawdzeniu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="097f4-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="097f4-694">Usunięto usterkę metody Concat</span><span class="sxs-lookup"><span data-stu-id="097f4-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-695">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-696">Poprawiono różne literówki w module</span><span class="sxs-lookup"><span data-stu-id="097f4-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-697">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-698">Usunięto usterkę polegającą na tym, że klient otrzymywał błąd „Nieprawidłowy ciąg Base-64” podczas używania polecenia cmdlet Get-AzHDInsightCluster do pobrania klastra za pomocą magazynu usługi ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="097f4-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="097f4-699">Dodano parametr o nazwie „ApplicationId” do trzech poleceń cmdlet: Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig i New-AzHDInsightCluster, aby klient mógł podać identyfikator aplikacji jednostki usługi na potrzeby uzyskiwania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="097f4-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="097f4-700">Zmieniono ustawienie Microsoft.Azure.Management.HDInsight z 2.1.0 na 5.1.0</span><span class="sxs-lookup"><span data-stu-id="097f4-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="097f4-701">Usunięto pięć poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="097f4-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="097f4-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="097f4-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="097f4-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="097f4-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="097f4-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="097f4-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="097f4-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="097f4-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="097f4-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="097f4-707">Dodano trzy polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="097f4-708">Get-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="097f4-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="097f4-709">Enable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="097f4-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="097f4-710">Disable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="097f4-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="097f4-711">Naprawiono polecenie cmdlet Get-AzHDInsightProperties w celu obsługi pobierania informacji o możliwościach z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="097f4-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="097f4-712">Usunięto zestawy parametrów („Spark1”, „Spark2”) z polecenia cmdlet Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="097f4-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="097f4-713">Dodano przykłady do dokumentów pomocy polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="097f4-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="097f4-714">Zmieniono typ danych wyjściowych następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="097f4-715">Typ danych wyjściowych polecenia cmdlet Get-AzHDInsightProperties zmieniono z CapabilitiesResponse na AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="097f4-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="097f4-716">Typ danych wyjściowych polecenia cmdlet Remove-AzHDInsightCluster zmieniono z ClusterGetResponse na bool.</span><span class="sxs-lookup"><span data-stu-id="097f4-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="097f4-717">Typ danych wyjściowych polecenia cmdlet Set-AzHDInsightGatewaySettings zmieniono z HttpConnectivitySettings na GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="097f4-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="097f4-718">Dodano kilka przypadków testowych scenariuszy.</span><span class="sxs-lookup"><span data-stu-id="097f4-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="097f4-719">Usunięto alias: „Add-AzHDInsightConfigValues”, „Get-AzHDInsightProperties”.</span><span class="sxs-lookup"><span data-stu-id="097f4-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-720">Az.IotHub</span></span>
* <span data-ttu-id="097f4-721">Zmiany powodujące niezgodność:</span><span class="sxs-lookup"><span data-stu-id="097f4-721">Breaking changes:</span></span>
    - <span data-ttu-id="097f4-722">Polecenie cmdlet „Add-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="097f4-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="097f4-723">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet Add-AzIotHubEventHubConsumerGroup został usunięty.</span><span class="sxs-lookup"><span data-stu-id="097f4-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="097f4-724">Polecenie cmdlet „Get-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="097f4-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="097f4-725">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Get-AzIotHubEventHubConsumerGroup” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="097f4-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="097f4-726">Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties” została usunięta.</span><span class="sxs-lookup"><span data-stu-id="097f4-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="097f4-727">Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties” została usunięta.</span><span class="sxs-lookup"><span data-stu-id="097f4-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="097f4-728">Polecenie cmdlet „New-AzIotHubExportDevice” nie obsługuje już aliasu „New-AzIotHubExportDevices”.</span><span class="sxs-lookup"><span data-stu-id="097f4-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="097f4-729">Polecenie cmdlet „New-AzIotHubImportDevice” nie obsługuje już aliasu „New-AzIotHubImportDevices”.</span><span class="sxs-lookup"><span data-stu-id="097f4-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="097f4-730">Polecenie cmdlet „Remove-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="097f4-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="097f4-731">Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Remove-AzIotHubEventHubConsumerGroup” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="097f4-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="097f4-732">Polecenie cmdlet „Set-AzIotHub” nie obsługuje już parametru „OperationsMonitoringProperties”, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="097f4-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="097f4-733">Zestaw parametrów „UpdateOperationsMonitoringProperties” dla polecenia cmdlet „Set-AzIotHub” został usunięty.</span><span class="sxs-lookup"><span data-stu-id="097f4-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-735">Obsługa przez usługę Azure Site Recovery konfigurowania zasobów sieciowych, takich jak sieciowa grupa zabezpieczeń, publiczny adres IP i wewnętrzne moduły równoważenia obciążenia, dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-736">Obsługa przez usługę Azure Site Recovery zapisu na dysku zarządzanym dla odzyskiwania z programu vMWare na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="097f4-737">Obsługa przez usługę Azure Site Recovery redukcji karty interfejsu sieciowego dla odzyskiwania z programu vMWare na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="097f4-738">Obsługa przez usługę Azure Site Recovery przyspieszonej sieci dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-739">Obsługa przez usługę Azure Site Recovery automatycznej aktualizacji agenta dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-740">Obsługa przez usługę Azure Site Recovery dysku SSD w warstwie Standardowa dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-741">Obsługa przez usługę Azure Site Recovery scenariusza dwuprzebiegowego usługi Azure Disk Encryption dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-742">Obsługa przez usługę Azure Site Recovery ochrony nowo dodanych dysków dla odzyskiwania z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-743">Dodano funkcję SoftDelete dla maszyny wirtualnej i dodano testy dla funkcji softdelete</span><span class="sxs-lookup"><span data-stu-id="097f4-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-744">Az.Resources</span></span>
* <span data-ttu-id="097f4-745">Aktualizacja zestawu zależnego Microsoft.Extensions.Caching.Memory z 1.1.1 do 2.2</span><span class="sxs-lookup"><span data-stu-id="097f4-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-746">Az.Network</span></span>
* <span data-ttu-id="097f4-747">Zmieniono wszystkie polecenia cmdlet dla klasy PrivateEndpointConnection w celu obsługi ogólnego dostawcy usług.</span><span class="sxs-lookup"><span data-stu-id="097f4-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="097f4-748">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="097f4-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="097f4-754">Dodano nowe polecenie cmdlet dla klasy PrivateLinkResource, które również obsługuje ogólnego dostawcę usług.</span><span class="sxs-lookup"><span data-stu-id="097f4-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="097f4-755">Nowe polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-755">New cmdlet:</span></span>
        - <span data-ttu-id="097f4-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="097f4-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="097f4-757">Dodano nowe pola i parametr dla funkcji protokołu proxy w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="097f4-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="097f4-758">Dodano właściwość EnableProxyProtocol w klasie PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="097f4-759">Dodano właściwość LinkIdentifier w klasie PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="097f4-760">Zaktualizowano polecenie cmdlet New-AzPrivateLinkService w celu dodania nowego opcjonalnego parametru EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="097f4-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="097f4-761">Poprawiono nieprawidłowy opis parametru w dokumentacji referencyjnej polecenia „New-AzApplicationGatewaySku”</span><span class="sxs-lookup"><span data-stu-id="097f4-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="097f4-762">Nowe polecenia cmdlet do obsługi zasad usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="097f4-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="097f4-763">Dodano obsługę zasobu podrzędnego RouteTables klasy VirtualHub</span><span class="sxs-lookup"><span data-stu-id="097f4-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="097f4-764">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-764">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="097f4-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="097f4-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="097f4-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="097f4-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="097f4-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="097f4-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="097f4-770">Dodano obsługę nowych właściwości Sku klasy VirtualHub i VirtualWANType klasy VirtualWan</span><span class="sxs-lookup"><span data-stu-id="097f4-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="097f4-771">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="097f4-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="097f4-772">New-AzVirtualHub: dodano parametr Sku</span><span class="sxs-lookup"><span data-stu-id="097f4-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="097f4-773">Update-AzVirtualHub: dodano parametr Sku</span><span class="sxs-lookup"><span data-stu-id="097f4-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="097f4-774">New-AzVirtualWan: dodano parametr VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="097f4-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="097f4-775">Update-AzVirtualWan: dodano parametr VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="097f4-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="097f4-776">Dodano obsługę właściwości EnableInternetSecurity dla klas HubVnetConnection, VpnConnection i ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="097f4-777">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-777">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="097f4-779">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="097f4-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="097f4-780">New-AzureRmVirtualHubVnetConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="097f4-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="097f4-781">New-AzureRmVpnConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="097f4-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="097f4-782">Update-AzureRmVpnConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="097f4-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="097f4-783">New-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="097f4-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="097f4-784">Set-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="097f4-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="097f4-785">Dodano obsługę konfigurowania zasad TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="097f4-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="097f4-786">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-786">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="097f4-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="097f4-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="097f4-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="097f4-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="097f4-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="097f4-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="097f4-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="097f4-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="097f4-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="097f4-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="097f4-793">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="097f4-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="097f4-794">New-AzApplicationGatewayFirewallPolicy: dodano parametr PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="097f4-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="097f4-795">Dodano obsługę operatora dopasowania geograficznego w obiekcie CustomRule</span><span class="sxs-lookup"><span data-stu-id="097f4-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="097f4-796">Dodano element GeoMatch do operatora w klasie FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="097f4-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="097f4-797">Dodano obsługę zasad zapory perListener i perSite</span><span class="sxs-lookup"><span data-stu-id="097f4-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="097f4-798">Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:</span><span class="sxs-lookup"><span data-stu-id="097f4-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="097f4-799">New-AzApplicationGatewayHttpListener: dodano parametr FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="097f4-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="097f4-800">New-AzApplicationGatewayPathRuleConfig: dodano parametr FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="097f4-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="097f4-801">Poprawka wymaganej podsieci o nazwie AzureBastionSubnet w elemencie „PSBastion” może ignorować wielkość liter</span><span class="sxs-lookup"><span data-stu-id="097f4-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="097f4-802">Obsługa docelowych nazw FQDN w regułach sieci i przetłumaczonej nazwy FQDN w regułach translatora adresów sieciowych dla usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="097f4-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="097f4-803">Dodano obsługę zasobu najwyższego poziomu RouteTables klasy IpGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="097f4-804">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-804">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="097f4-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="097f4-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="097f4-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-810">Usunięto polecenie cmdlet Add-AzServiceFabricApplicationCertificate, ponieważ ten scenariusz jest objęty poleceniem Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="097f4-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-811">Az.Sql</span></span>
* <span data-ttu-id="097f4-812">Dodano obsługę przywracania porzuconych baz danych w wystąpieniach zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="097f4-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="097f4-813">Oznaczono jako przestarzałe w kodzie stare polecenia cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="097f4-814">Usunięto przestarzałe aliasy:</span><span class="sxs-lookup"><span data-stu-id="097f4-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="097f4-815">Get-AzSqlDatabaseIndexRecommendations (zamiast tego użyj Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="097f4-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="097f4-816">Get-AzSqlDatabaseRestorePoints (zamiast tego użyj Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="097f4-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="097f4-817">Usunięto polecenie cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="097f4-818">Usunięto aliasy dla przestarzałych poleceń cmdlet ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="097f4-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="097f4-819">Oznaczono jako przestarzałe polecenia cmdlet ustawień zaawansowanego wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="097f4-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="097f4-820">Dodawanie poleceń cmdlet do wyłączania i włączania zaleceń dotyczących czułości dla kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="097f4-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-821">Az.Storage</span></span>
* <span data-ttu-id="097f4-822">Obsługa włączania dużego udziału plików podczas tworzenia lub aktualizowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="097f4-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="097f4-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="097f4-825">Podczas zamykania/uzyskiwania dojścia do pliku pomiń sprawdzanie, czy ścieżka danych wejściowych jest ścieżką pliku, czy plikiem, aby uniknąć błędu obiektu w stanie DeletePending</span><span class="sxs-lookup"><span data-stu-id="097f4-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="097f4-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="097f4-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="097f4-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="097f4-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="097f4-828">2.8.0 — październik 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="097f4-829">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-829">General</span></span>
* <span data-ttu-id="097f4-830">Wydanie Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-831">Az.Accounts</span></span>
* <span data-ttu-id="097f4-832">Aktualizacja telemetrii i ponowne zapisywanie adresów URL dla wygenerowanych modułów oraz naprawa testów jednostkowych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="097f4-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-833">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-834">**Set-AzApiManagementApi** — Dodano obsługę aktualizowania interfejsu API do właściwości ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="097f4-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="097f4-835">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="097f4-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-836">Az.Automation</span></span>
* <span data-ttu-id="097f4-837">Naprawiono parametr ponownego uruchamiania polecenia cmdlet New-AzureAutomationSoftwareUpdateConfiguration dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="097f4-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="097f4-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-838">Az.Batch</span></span>
* <span data-ttu-id="097f4-839">Polecenie **Get-AzBatchNodeAgentSku** jest przestarzałe i zostanie zastąpione poleceniem **Get-AzBatchSupportImage** w wersji 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="097f4-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-840">Az.Compute</span></span>
* <span data-ttu-id="097f4-841">Dodano parametry Priority, EvictionPolicy i MaxPrice do poleceń cmdlet New-AzVM i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="097f4-842">Naprawiono komunikat ostrzegawczy i dokumentację pomocy dla poleceń Add-AzVMAdditionalUnattendContent i Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="097f4-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="097f4-843">Naprawiono wyjątek -skipVmBackup dla maszyn wirtualnych z systemem Linux z dyskami zarządzanymi dla polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="097f4-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="097f4-844">Naprawiono usterkę w ustawieniach szyfrowania aktualizacji w scenariuszu dwuprzebiegowym polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="097f4-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-845">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-846">Dodano polecenia CRUD dla przepływu danych usługi ADF w wersji 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow i Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="097f4-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="097f4-847">Dodano polecenia akcji dla sesji debugowania przepływu danych usługi ADF w wersji 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand i Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="097f4-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="097f4-848">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.2.0</span><span class="sxs-lookup"><span data-stu-id="097f4-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-850">Naprawiono weryfikację kont, aby umożliwić przekazywanie kont ze znakiem „-” bez domeny</span><span class="sxs-lookup"><span data-stu-id="097f4-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="097f4-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="097f4-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="097f4-852">Zaktualizowano program PowerShell do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="097f4-853">Zaktualizowano zestaw SDK do wersji 1.0.2</span><span class="sxs-lookup"><span data-stu-id="097f4-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="097f4-854">Zaktualizowano testy, aby odwoływały się do nowej wersji zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="097f4-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="097f4-855">Zaktualizowano strukturę wyjściową z zagnieżdżonej do spłaszczonej.</span><span class="sxs-lookup"><span data-stu-id="097f4-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-856">Az.IotHub</span></span>
* <span data-ttu-id="097f4-857">Dodano nowe źródło routingu: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="097f4-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="097f4-858">Drobna poprawka usterki: Polecenie Get-AzIothub nie zwraca wartości subscriptionId</span><span class="sxs-lookup"><span data-stu-id="097f4-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-859">Az.Monitor</span></span>
* <span data-ttu-id="097f4-860">Dodano nowe odbiorniki grupy akcji dla grupy akcji -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="097f4-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="097f4-861">Włączono korzystanie z typowych schematów alertów dla odbiorników.</span><span class="sxs-lookup"><span data-stu-id="097f4-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="097f4-862">Nie dotyczy to odbiorników wiadomości SMS, powiadomień push usługi Azure App , narzędzia ITSM i połączeń głosowych</span><span class="sxs-lookup"><span data-stu-id="097f4-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="097f4-863">Elementy webhook obsługują teraz również uwierzytelnianie za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="097f4-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-864">Az.Network</span></span>
* <span data-ttu-id="097f4-865">Dodano nowe polecenie cmdlet Get-AzAvailableServiceAlias, które można wywołać, aby pobrać aliasy do użytku z zasadami punktu końcowego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="097f4-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="097f4-866">Dodano obsługę dodawania selektorów ruchu do połączeń bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="097f4-867">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-867">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="097f4-869">Polecenia cmdlet zostały zaktualizowane o opcjonalny parametr -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="097f4-870">Dodano obsługę protokołów ESP i AH do konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="097f4-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="097f4-871">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="097f4-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="097f4-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="097f4-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="097f4-875">Poprawiono obsługę wyjątków w poleceniach cmdlet usługi Cortex</span><span class="sxs-lookup"><span data-stu-id="097f4-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="097f4-876">Dodano nowe generacje i jednostki SKU dla elementów VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="097f4-877">Wprowadzono nowe generacje dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="097f4-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="097f4-878">Wprowadzono nowe jednostki SKU o wysokiej przepływności dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="097f4-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="097f4-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="097f4-879">Az.RedisCache</span></span>
* <span data-ttu-id="097f4-880">Zaktualizowano dokumentację referencyjną polecenia „Set-AzRedisCache” w celu uwzględnienia brakujących wartości parametru „-Size”</span><span class="sxs-lookup"><span data-stu-id="097f4-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-881">Az.Sql</span></span>
* <span data-ttu-id="097f4-882">Dodano obsługę ustawiania administratora usługi Active Directory w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="097f4-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-883">Az.Storage</span></span>
* <span data-ttu-id="097f4-884">Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 11.1.0</span><span class="sxs-lookup"><span data-stu-id="097f4-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="097f4-885">Utworzenie listy kontenerów przy użyciu interfejsu API płaszczyzny zarządzania spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="097f4-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="097f4-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="097f4-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="097f4-887">Utworzenie listy kont magazynu z subskrypcji spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="097f4-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="097f4-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="097f4-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="097f4-889">Az.StorageSync</span></span>
* <span data-ttu-id="097f4-890">Naprawiono problem 9810 w poleceniu Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="097f4-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-891">Az.Websites</span></span>
* <span data-ttu-id="097f4-892">Aktualizowanie elementu ASP aplikacji przy użyciu polecenia Set-AzWebApp kończyło się niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="097f4-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="097f4-893">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="097f4-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-894">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-895">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="097f4-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="097f4-896">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="097f4-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="097f4-897">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="097f4-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-898">Az.Automation</span></span>
* <span data-ttu-id="097f4-899">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="097f4-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="097f4-900">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="097f4-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="097f4-901">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="097f4-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-902">Az.Compute</span></span>
* <span data-ttu-id="097f4-903">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="097f4-904">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="097f4-905">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="097f4-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="097f4-906">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="097f4-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="097f4-907">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="097f4-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="097f4-908">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="097f4-909">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="097f4-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="097f4-910">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="097f4-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="097f4-911">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="097f4-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-912">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-913">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="097f4-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="097f4-914">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="097f4-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-915">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-916">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="097f4-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-917">Az.IotHub</span></span>
* <span data-ttu-id="097f4-918">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="097f4-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="097f4-919">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="097f4-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="097f4-920">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-920">New cmdlets are:</span></span>
    - <span data-ttu-id="097f4-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="097f4-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="097f4-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="097f4-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="097f4-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="097f4-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="097f4-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="097f4-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-925">Az.Monitor</span></span>
* <span data-ttu-id="097f4-926">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="097f4-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="097f4-927">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="097f4-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="097f4-928">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="097f4-929">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="097f4-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="097f4-930">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="097f4-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="097f4-931">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="097f4-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="097f4-932">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="097f4-933">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="097f4-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="097f4-934">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="097f4-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="097f4-935">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="097f4-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="097f4-936">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="097f4-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="097f4-937">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="097f4-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="097f4-938">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="097f4-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="097f4-939">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="097f4-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="097f4-940">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="097f4-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="097f4-941">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="097f4-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="097f4-942">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="097f4-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="097f4-943">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="097f4-944">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="097f4-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="097f4-945">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-945">Overall improved help files</span></span>
* <span data-ttu-id="097f4-946">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="097f4-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-947">Az.Network</span></span>
* <span data-ttu-id="097f4-948">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="097f4-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="097f4-949">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="097f4-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="097f4-950">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="097f4-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="097f4-951">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="097f4-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="097f4-952">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="097f4-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="097f4-953">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="097f4-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="097f4-954">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="097f4-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="097f4-955">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="097f4-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="097f4-956">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="097f4-957">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="097f4-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="097f4-958">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="097f4-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="097f4-959">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="097f4-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="097f4-960">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-960">New cmdlets</span></span>
        - <span data-ttu-id="097f4-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="097f4-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="097f4-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="097f4-963">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="097f4-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="097f4-964">New-VpnSite</span></span>
        - <span data-ttu-id="097f4-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="097f4-965">Update-VpnSite</span></span>
        - <span data-ttu-id="097f4-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-966">New-VpnConnection</span></span>
        - <span data-ttu-id="097f4-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-967">Update-VpnConnection</span></span>
* <span data-ttu-id="097f4-968">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="097f4-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-970">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="097f4-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="097f4-971">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-972">Az.Resources</span></span>
* <span data-ttu-id="097f4-973">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="097f4-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-975">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="097f4-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="097f4-976">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="097f4-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="097f4-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="097f4-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="097f4-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="097f4-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="097f4-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="097f4-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="097f4-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="097f4-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="097f4-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="097f4-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="097f4-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="097f4-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="097f4-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="097f4-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="097f4-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="097f4-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="097f4-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="097f4-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="097f4-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="097f4-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="097f4-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="097f4-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="097f4-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="097f4-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="097f4-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="097f4-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="097f4-990">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="097f4-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="097f4-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="097f4-991">Az.SignalR</span></span>
* <span data-ttu-id="097f4-992">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="097f4-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-993">Az.Sql</span></span>
* <span data-ttu-id="097f4-994">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="097f4-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="097f4-995">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="097f4-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="097f4-996">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="097f4-997">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="097f4-998">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="097f4-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-999">Az.Storage</span></span>
* <span data-ttu-id="097f4-1000">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="097f4-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="097f4-1001">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="097f4-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="097f4-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="097f4-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="097f4-1004">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="097f4-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="097f4-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="097f4-1006">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="097f4-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="097f4-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="097f4-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="097f4-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="097f4-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="097f4-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1011">Az.Websites</span></span>
* <span data-ttu-id="097f4-1012">Naprawa problemu polegającego na tym, że tagi webapp były usuwane podczas migracji aplikacji do nowej platformy ASP</span><span class="sxs-lookup"><span data-stu-id="097f4-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="097f4-1013">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="097f4-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="097f4-1014">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="097f4-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="097f4-1015">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="097f4-1016">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-1016">General</span></span>
* <span data-ttu-id="097f4-1017">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="097f4-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1018">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1019">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="097f4-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="097f4-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="097f4-1020">Az.Aks</span></span>
* <span data-ttu-id="097f4-1021">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="097f4-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="097f4-1022">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="097f4-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-1024">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="097f4-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="097f4-1025">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="097f4-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="097f4-1026">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="097f4-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="097f4-1027">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="097f4-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="097f4-1028">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="097f4-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="097f4-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-1029">Az.Batch</span></span>
* <span data-ttu-id="097f4-1030">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="097f4-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-1031">Az.Cdn</span></span>
* <span data-ttu-id="097f4-1032">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="097f4-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1033">Az.Compute</span></span>
* <span data-ttu-id="097f4-1034">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="097f4-1035">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="097f4-1036">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="097f4-1037">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="097f4-1038">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="097f4-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="097f4-1039">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="097f4-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="097f4-1040">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="097f4-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="097f4-1041">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="097f4-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1042">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1043">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="097f4-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="097f4-1044">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="097f4-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="097f4-1045">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="097f4-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="097f4-1046">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="097f4-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1048">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="097f4-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1049">Az.EventHub</span></span>
* <span data-ttu-id="097f4-1050">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="097f4-1051">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="097f4-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="097f4-1052">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="097f4-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="097f4-1053">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="097f4-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="097f4-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="097f4-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="097f4-1055">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="097f4-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-1056">Az.Monitor</span></span>
* <span data-ttu-id="097f4-1057">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1058">Az.Network</span></span>
* <span data-ttu-id="097f4-1059">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="097f4-1060">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="097f4-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="097f4-1061">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="097f4-1062">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="097f4-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="097f4-1063">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="097f4-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="097f4-1064">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="097f4-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="097f4-1065">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="097f4-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1067">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="097f4-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="097f4-1068">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="097f4-1068">Added example</span></span>
    - <span data-ttu-id="097f4-1069">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="097f4-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="097f4-1070">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="097f4-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="097f4-1071">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="097f4-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1073">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1074">Az.Resources</span></span>
* <span data-ttu-id="097f4-1075">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="097f4-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="097f4-1076">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="097f4-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="097f4-1077">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="097f4-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="097f4-1078">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="097f4-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-1080">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="097f4-1081">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="097f4-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="097f4-1082">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="097f4-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-1084">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="097f4-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="097f4-1085">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="097f4-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="097f4-1086">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="097f4-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="097f4-1087">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="097f4-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="097f4-1088">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="097f4-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="097f4-1089">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="097f4-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1090">Az.Sql</span></span>
* <span data-ttu-id="097f4-1091">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1092">Az.Storage</span></span>
* <span data-ttu-id="097f4-1093">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="097f4-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="097f4-1094">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="097f4-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="097f4-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="097f4-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="097f4-1097">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="097f4-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="097f4-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1099">Az.Websites</span></span>
* <span data-ttu-id="097f4-1100">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="097f4-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="097f4-1101">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="097f4-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1102">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1103">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="097f4-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="097f4-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="097f4-1105">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="097f4-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1106">Az.Automation</span></span>
* <span data-ttu-id="097f4-1107">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="097f4-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-1109">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="097f4-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1110">Az.Compute</span></span>
* <span data-ttu-id="097f4-1111">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="097f4-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="097f4-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="097f4-1113">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="097f4-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="097f4-1114">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="097f4-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1115">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1116">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="097f4-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="097f4-1117">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="097f4-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1118">Az.EventHub</span></span>
* <span data-ttu-id="097f4-1119">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="097f4-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="097f4-1120">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="097f4-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1121">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-1122">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="097f4-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="097f4-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1123">Az.LogicApp</span></span>
* <span data-ttu-id="097f4-1124">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="097f4-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="097f4-1125">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="097f4-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="097f4-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="097f4-1127">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="097f4-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1128">Az.Network</span></span>
* <span data-ttu-id="097f4-1129">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="097f4-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="097f4-1130">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1130">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="097f4-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="097f4-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="097f4-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="097f4-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="097f4-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="097f4-1139">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="097f4-1140">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="097f4-1141">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="097f4-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="097f4-1142">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="097f4-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="097f4-1143">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="097f4-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="097f4-1144">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="097f4-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="097f4-1145">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="097f4-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="097f4-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="097f4-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="097f4-1149">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="097f4-1150">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="097f4-1151">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="097f4-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="097f4-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="097f4-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="097f4-1155">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="097f4-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="097f4-1156">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="097f4-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="097f4-1157">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="097f4-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1159">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="097f4-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="097f4-1160">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="097f4-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1162">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="097f4-1163">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="097f4-1164">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="097f4-1165">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="097f4-1166">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="097f4-1167">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="097f4-1168">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="097f4-1169">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="097f4-1170">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="097f4-1171">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="097f4-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1172">Az.Resources</span></span>
- <span data-ttu-id="097f4-1173">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="097f4-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="097f4-1174">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="097f4-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-1176">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="097f4-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="097f4-1177">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="097f4-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1178">Az.Sql</span></span>
* <span data-ttu-id="097f4-1179">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="097f4-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="097f4-1180">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="097f4-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="097f4-1181">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="097f4-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1182">Az.Storage</span></span>
* <span data-ttu-id="097f4-1183">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="097f4-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="097f4-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="097f4-1184">Az.StorageSync</span></span>
* <span data-ttu-id="097f4-1185">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="097f4-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="097f4-1186">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="097f4-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1187">Az.Websites</span></span>
* <span data-ttu-id="097f4-1188">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="097f4-1189">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="097f4-1190">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="097f4-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="097f4-1191">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1192">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1193">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="097f4-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="097f4-1194">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="097f4-1195">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="097f4-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="097f4-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="097f4-1196">Az.Advisor</span></span>
* <span data-ttu-id="097f4-1197">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="097f4-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="097f4-1198">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="097f4-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="097f4-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-1200">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="097f4-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="097f4-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="097f4-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="097f4-1202">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="097f4-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="097f4-1203">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="097f4-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="097f4-1204">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="097f4-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="097f4-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="097f4-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="097f4-1206">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="097f4-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1207">Az.Automation</span></span>
* <span data-ttu-id="097f4-1208">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="097f4-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1209">Az.Compute</span></span>
* <span data-ttu-id="097f4-1210">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1211">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1212">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="097f4-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="097f4-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="097f4-1213">Az.EventGrid</span></span>
* <span data-ttu-id="097f4-1214">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="097f4-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1215">Az.IotHub</span></span>
* <span data-ttu-id="097f4-1216">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="097f4-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1217">Az.Network</span></span>
* <span data-ttu-id="097f4-1218">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="097f4-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="097f4-1219">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="097f4-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-1221">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="097f4-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="097f4-1222">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="097f4-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1224">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="097f4-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1226">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="097f4-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1227">Az.Resources</span></span>
    - <span data-ttu-id="097f4-1228">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="097f4-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="097f4-1229">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="097f4-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="097f4-1230">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="097f4-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="097f4-1231">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="097f4-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-1233">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="097f4-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1234">Az.Sql</span></span>
* <span data-ttu-id="097f4-1235">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="097f4-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="097f4-1236">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="097f4-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="097f4-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="097f4-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="097f4-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="097f4-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="097f4-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="097f4-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="097f4-1243">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="097f4-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1244">Az.Storage</span></span>
* <span data-ttu-id="097f4-1245">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="097f4-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="097f4-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="097f4-1247">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="097f4-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="097f4-1248">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="097f4-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="097f4-1249">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="097f4-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="097f4-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="097f4-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="097f4-1252">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="097f4-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="097f4-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="097f4-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="097f4-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="097f4-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="097f4-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="097f4-1255">Az.StorageSync</span></span>
* <span data-ttu-id="097f4-1256">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="097f4-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="097f4-1257">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1258">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1259">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="097f4-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="097f4-1260">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="097f4-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="097f4-1261">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="097f4-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="097f4-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="097f4-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="097f4-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="097f4-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1264">Az.Compute</span></span>
* <span data-ttu-id="097f4-1265">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="097f4-1266">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="097f4-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="097f4-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="097f4-1267">Az.Dns</span></span>
* <span data-ttu-id="097f4-1268">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="097f4-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="097f4-1269">Az.EventGrid</span></span>
* <span data-ttu-id="097f4-1270">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="097f4-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="097f4-1271">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1271">New cmdlets:</span></span>
    - <span data-ttu-id="097f4-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="097f4-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="097f4-1273">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="097f4-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="097f4-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="097f4-1275">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="097f4-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="097f4-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="097f4-1277">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="097f4-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="097f4-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="097f4-1279">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="097f4-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="097f4-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="097f4-1281">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="097f4-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="097f4-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="097f4-1283">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="097f4-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="097f4-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="097f4-1285">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="097f4-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="097f4-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="097f4-1287">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="097f4-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="097f4-1288">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="097f4-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="097f4-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="097f4-1290">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="097f4-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="097f4-1291">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="097f4-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="097f4-1292">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="097f4-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="097f4-1293">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="097f4-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="097f4-1294">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="097f4-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="097f4-1295">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="097f4-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="097f4-1296">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="097f4-1297">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="097f4-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="097f4-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="097f4-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="097f4-1299">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="097f4-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="097f4-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="097f4-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="097f4-1301">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="097f4-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="097f4-1302">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="097f4-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="097f4-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="097f4-1305">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="097f4-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="097f4-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="097f4-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="097f4-1307">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="097f4-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1308">Az.Network</span></span>
* <span data-ttu-id="097f4-1309">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="097f4-1310">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1310">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="097f4-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="097f4-1312">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="097f4-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="097f4-1313">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1313">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="097f4-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="097f4-1315">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="097f4-1316">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1316">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="097f4-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="097f4-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="097f4-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="097f4-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="097f4-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="097f4-1322">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="097f4-1323">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1323">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="097f4-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="097f4-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="097f4-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="097f4-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="097f4-1328">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="097f4-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="097f4-1329">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="097f4-1330">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="097f4-1331">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="097f4-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="097f4-1332">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="097f4-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="097f4-1333">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="097f4-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="097f4-1334">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="097f4-1335">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="097f4-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="097f4-1336">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="097f4-1337">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="097f4-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="097f4-1338">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="097f4-1339">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="097f4-1340">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="097f4-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="097f4-1341">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="097f4-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="097f4-1342">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="097f4-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="097f4-1343">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="097f4-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="097f4-1344">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="097f4-1345">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="097f4-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="097f4-1346">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="097f4-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="097f4-1347">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="097f4-1348">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="097f4-1349">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="097f4-1350">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="097f4-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1352">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="097f4-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1353">Az.Resources</span></span>
* <span data-ttu-id="097f4-1354">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="097f4-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="097f4-1355">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="097f4-1356">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="097f4-1357">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="097f4-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-1359">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="097f4-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1360">Az.Sql</span></span>
* <span data-ttu-id="097f4-1361">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="097f4-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="097f4-1362">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="097f4-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="097f4-1363">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="097f4-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="097f4-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="097f4-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="097f4-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="097f4-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="097f4-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="097f4-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="097f4-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="097f4-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="097f4-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="097f4-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1369">Az.Storage</span></span>
* <span data-ttu-id="097f4-1370">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="097f4-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="097f4-1372">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="097f4-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="097f4-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1374">Az.Websites</span></span>
* <span data-ttu-id="097f4-1375">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="097f4-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="097f4-1376">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="097f4-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="097f4-1377">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="097f4-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-1378">Az.Cdn</span></span>
* <span data-ttu-id="097f4-1379">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="097f4-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1380">Az.Compute</span></span>
* <span data-ttu-id="097f4-1381">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="097f4-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="097f4-1382">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="097f4-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1383">Az.EventHub</span></span>
* <span data-ttu-id="097f4-1384">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="097f4-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="097f4-1385">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097f4-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1386">Az.Network</span></span>
* <span data-ttu-id="097f4-1387">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="097f4-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="097f4-1388">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="097f4-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-1390">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="097f4-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1392">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="097f4-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-1394">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097f4-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-1396">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="097f4-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="097f4-1397">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1398">Az.Sql</span></span>
* <span data-ttu-id="097f4-1399">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="097f4-1400">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="097f4-1401">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="097f4-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="097f4-1402">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="097f4-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1403">Az.Websites</span></span>
* <span data-ttu-id="097f4-1404">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="097f4-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="097f4-1405">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="097f4-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-1407">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="097f4-1408">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="097f4-1409">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="097f4-1410">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="097f4-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="097f4-1411">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="097f4-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="097f4-1412">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="097f4-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="097f4-1413">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="097f4-1414">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="097f4-1415">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="097f4-1416">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="097f4-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="097f4-1417">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="097f4-1418">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="097f4-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="097f4-1419">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="097f4-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="097f4-1420">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="097f4-1421">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="097f4-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="097f4-1422">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="097f4-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="097f4-1423">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="097f4-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="097f4-1424">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="097f4-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="097f4-1425">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="097f4-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="097f4-1426">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="097f4-1427">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="097f4-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="097f4-1428">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="097f4-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="097f4-1429">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="097f4-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="097f4-1430">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="097f4-1431">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="097f4-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="097f4-1432">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="097f4-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="097f4-1433">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="097f4-1434">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="097f4-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="097f4-1435">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="097f4-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="097f4-1436">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="097f4-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="097f4-1437">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="097f4-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="097f4-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="097f4-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="097f4-1439">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="097f4-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="097f4-1440">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="097f4-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="097f4-1441">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="097f4-1442">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="097f4-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="097f4-1443">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="097f4-1444">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="097f4-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="097f4-1445">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="097f4-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="097f4-1446">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="097f4-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="097f4-1447">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="097f4-1448">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="097f4-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="097f4-1449">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="097f4-1450">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="097f4-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="097f4-1451">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="097f4-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="097f4-1452">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="097f4-1453">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="097f4-1454">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="097f4-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="097f4-1455">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="097f4-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="097f4-1456">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="097f4-1457">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="097f4-1458">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="097f4-1459">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="097f4-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="097f4-1460">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="097f4-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="097f4-1461">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="097f4-1462">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="097f4-1463">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="097f4-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="097f4-1464">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="097f4-1465">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="097f4-1466">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="097f4-1467">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="097f4-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="097f4-1468">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="097f4-1469">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="097f4-1470">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="097f4-1471">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="097f4-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="097f4-1472">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="097f4-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="097f4-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="097f4-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="097f4-1474">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="097f4-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="097f4-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="097f4-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="097f4-1476">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="097f4-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="097f4-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="097f4-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="097f4-1478">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="097f4-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="097f4-1479">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="097f4-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="097f4-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="097f4-1481">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="097f4-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="097f4-1482">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="097f4-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="097f4-1483">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="097f4-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1484">Az.Automation</span></span>
* <span data-ttu-id="097f4-1485">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="097f4-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="097f4-1486">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="097f4-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="097f4-1487">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="097f4-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="097f4-1488">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="097f4-1489">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="097f4-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="097f4-1490">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="097f4-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="097f4-1491">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="097f4-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1492">Az.Compute</span></span>
* <span data-ttu-id="097f4-1493">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="097f4-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="097f4-1494">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="097f4-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1496">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-1497">Az.Monitor</span></span>
* <span data-ttu-id="097f4-1498">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1499">Az.Network</span></span>
* <span data-ttu-id="097f4-1500">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="097f4-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="097f4-1501">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="097f4-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="097f4-1503">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="097f4-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1504">Az.Resources</span></span>
* <span data-ttu-id="097f4-1505">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="097f4-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1506">Az.Sql</span></span>
* <span data-ttu-id="097f4-1507">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="097f4-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="097f4-1508">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1509">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1510">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="097f4-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-1512">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="097f4-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="097f4-1513">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="097f4-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1514">Az.Compute</span></span>
* <span data-ttu-id="097f4-1515">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="097f4-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="097f4-1516">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="097f4-1517">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="097f4-1518">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="097f4-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="097f4-1519">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="097f4-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="097f4-1520">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="097f4-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="097f4-1521">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="097f4-1521">Breaking changes</span></span>
    - <span data-ttu-id="097f4-1522">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="097f4-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="097f4-1523">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="097f4-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="097f4-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="097f4-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="097f4-1525">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="097f4-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="097f4-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="097f4-1526">Az.Dns</span></span>
* <span data-ttu-id="097f4-1527">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="097f4-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="097f4-1528">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="097f4-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="097f4-1529">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="097f4-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="097f4-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="097f4-1531">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="097f4-1532">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="097f4-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="097f4-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-1533">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-1534">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="097f4-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="097f4-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="097f4-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="097f4-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="097f4-1537">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="097f4-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="097f4-1538">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="097f4-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="097f4-1539">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="097f4-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="097f4-1540">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="097f4-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-1541">Az.Monitor</span></span>
* <span data-ttu-id="097f4-1542">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="097f4-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="097f4-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="097f4-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="097f4-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="097f4-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="097f4-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="097f4-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="097f4-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="097f4-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="097f4-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="097f4-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="097f4-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="097f4-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="097f4-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="097f4-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="097f4-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="097f4-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="097f4-1554">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="097f4-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="097f4-1555">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="097f4-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1556">Az.Network</span></span>
* <span data-ttu-id="097f4-1557">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="097f4-1558">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1558">New cmdlets</span></span>
        - <span data-ttu-id="097f4-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="097f4-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="097f4-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="097f4-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="097f4-1563">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="097f4-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="097f4-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="097f4-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="097f4-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="097f4-1566">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="097f4-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="097f4-1567">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="097f4-1568">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-1570">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="097f4-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="097f4-1571">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="097f4-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="097f4-1572">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="097f4-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1574">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="097f4-1575">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="097f4-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="097f4-1576">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="097f4-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="097f4-1577">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="097f4-1578">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="097f4-1579">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="097f4-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="097f4-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="097f4-1580">Az.Relay</span></span>
* <span data-ttu-id="097f4-1581">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="097f4-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-1583">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="097f4-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1584">Az.Storage</span></span>
* <span data-ttu-id="097f4-1585">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="097f4-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="097f4-1586">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="097f4-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="097f4-1587">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="097f4-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="097f4-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="097f4-1589">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="097f4-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="097f4-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="097f4-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="097f4-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1593">Az.Websites</span></span>
* <span data-ttu-id="097f4-1594">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="097f4-1595">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="097f4-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="097f4-1596">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-1597">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-1598">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="097f4-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="097f4-1599">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="097f4-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="097f4-1600">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="097f4-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="097f4-1601">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="097f4-1602">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="097f4-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="097f4-1603">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="097f4-1604">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1605">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1606">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="097f4-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="097f4-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-1607">Az.Batch</span></span>
* <span data-ttu-id="097f4-1608">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-1609">Az.Cdn</span></span>
* <span data-ttu-id="097f4-1610">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-1612">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1613">Az.Compute</span></span>
* <span data-ttu-id="097f4-1614">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="097f4-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="097f4-1615">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1616">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1617">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1618">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="097f4-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1620">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="097f4-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="097f4-1621">Az.EventGrid</span></span>
* <span data-ttu-id="097f4-1622">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="097f4-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1623">Az.EventHub</span></span>
* <span data-ttu-id="097f4-1624">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="097f4-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="097f4-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="097f4-1625">Az.HDInsight</span></span>
* <span data-ttu-id="097f4-1626">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1627">Az.IotHub</span></span>
* <span data-ttu-id="097f4-1628">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1629">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-1630">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1631">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="097f4-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="097f4-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="097f4-1633">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="097f4-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="097f4-1634">Az.Media</span></span>
* <span data-ttu-id="097f4-1635">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-1636">Az.Monitor</span></span>
  * <span data-ttu-id="097f4-1637">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="097f4-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="097f4-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="097f4-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="097f4-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="097f4-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="097f4-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="097f4-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="097f4-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="097f4-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="097f4-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="097f4-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="097f4-1643">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="097f4-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1644">Az.Network</span></span>
* <span data-ttu-id="097f4-1645">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1646">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="097f4-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="097f4-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="097f4-1648">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1650">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="097f4-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="097f4-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="097f4-1652">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1654">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1655">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="097f4-1656">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="097f4-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="097f4-1657">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="097f4-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="097f4-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="097f4-1658">Az.RedisCache</span></span>
* <span data-ttu-id="097f4-1659">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1660">Az.Resources</span></span>
* <span data-ttu-id="097f4-1661">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1662">Az.Sql</span></span>
* <span data-ttu-id="097f4-1663">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="097f4-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="097f4-1664">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1665">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="097f4-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="097f4-1666">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="097f4-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="097f4-1667">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="097f4-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="097f4-1668">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="097f4-1669">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1670">Az.Websites</span></span>
* <span data-ttu-id="097f4-1671">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="097f4-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="097f4-1672">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="097f4-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="097f4-1673">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="097f4-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="097f4-1674">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="097f4-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="097f4-1675">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-1676">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-1677">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="097f4-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="097f4-1678">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="097f4-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="097f4-1679">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="097f4-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="097f4-1680">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="097f4-1681">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="097f4-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="097f4-1682">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="097f4-1683">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="097f4-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1684">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1685">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="097f4-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="097f4-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="097f4-1687">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="097f4-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="097f4-1688">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="097f4-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1689">Az.Automation</span></span>
* <span data-ttu-id="097f4-1690">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="097f4-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="097f4-1691">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="097f4-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="097f4-1692">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1693">Az.Compute</span></span>
* <span data-ttu-id="097f4-1694">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="097f4-1695">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="097f4-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="097f4-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="097f4-1697">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="097f4-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1698">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1699">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="097f4-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="097f4-1700">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="097f4-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1701">Az.Resources</span></span>
* <span data-ttu-id="097f4-1702">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="097f4-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="097f4-1703">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="097f4-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="097f4-1704">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="097f4-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="097f4-1705">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="097f4-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="097f4-1706">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="097f4-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="097f4-1707">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="097f4-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1708">Az.Sql</span></span>
* <span data-ttu-id="097f4-1709">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="097f4-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1710">Az.Storage</span></span>
* <span data-ttu-id="097f4-1711">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="097f4-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="097f4-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="097f4-1713">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="097f4-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="097f4-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="097f4-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="097f4-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="097f4-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="097f4-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="097f4-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="097f4-1718">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="097f4-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="097f4-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="097f4-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="097f4-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="097f4-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="097f4-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="097f4-1723">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="097f4-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="097f4-1724">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="097f4-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="097f4-1725">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="097f4-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="097f4-1726">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="097f4-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="097f4-1727">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="097f4-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="097f4-1728">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="097f4-1729">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="097f4-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="097f4-1730">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="097f4-1731">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1732">Az.Automation</span></span>
* <span data-ttu-id="097f4-1733">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="097f4-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="097f4-1734">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="097f4-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="097f4-1735">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="097f4-1735">Pre-Post script</span></span>
    * <span data-ttu-id="097f4-1736">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="097f4-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1737">Az.Compute</span></span>
* <span data-ttu-id="097f4-1738">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="097f4-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="097f4-1739">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="097f4-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1740">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-1741">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1742">Az.Network</span></span>
* <span data-ttu-id="097f4-1743">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="097f4-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="097f4-1744">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="097f4-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1746">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="097f4-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="097f4-1747">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="097f4-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1748">Az.Resources</span></span>
* <span data-ttu-id="097f4-1749">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="097f4-1750">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="097f4-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1751">Az.Sql</span></span>
* <span data-ttu-id="097f4-1752">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="097f4-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1753">Az.Storage</span></span>
* <span data-ttu-id="097f4-1754">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="097f4-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="097f4-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="097f4-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="097f4-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="097f4-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="097f4-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="097f4-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="097f4-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="097f4-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1761">Az.Websites</span></span>
* <span data-ttu-id="097f4-1762">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="097f4-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="097f4-1763">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="097f4-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1764">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1765">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="097f4-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="097f4-1766">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1767">Az.Automation</span></span>
* <span data-ttu-id="097f4-1768">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="097f4-1769">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="097f4-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="097f4-1770">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="097f4-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-1771">Az.Cdn</span></span>
* <span data-ttu-id="097f4-1772">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="097f4-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1773">Az.Compute</span></span>
* <span data-ttu-id="097f4-1774">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="097f4-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1775">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1776">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="097f4-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="097f4-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1777">Az.LogicApp</span></span>
* <span data-ttu-id="097f4-1778">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="097f4-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1779">Az.Network</span></span>
* <span data-ttu-id="097f4-1780">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="097f4-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1782">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="097f4-1783">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="097f4-1783">SDK Update</span></span>
* <span data-ttu-id="097f4-1784">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="097f4-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="097f4-1785">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="097f4-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1786">Az.Resources</span></span>
* <span data-ttu-id="097f4-1787">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="097f4-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="097f4-1788">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="097f4-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="097f4-1789">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="097f4-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="097f4-1790">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="097f4-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="097f4-1791">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="097f4-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="097f4-1792">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="097f4-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1793">Az.Sql</span></span>
* <span data-ttu-id="097f4-1794">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="097f4-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="097f4-1795">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="097f4-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1796">Az.Storage</span></span>
* <span data-ttu-id="097f4-1797">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="097f4-1798">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="097f4-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="097f4-1800">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1801">Az.Automation</span></span>
* <span data-ttu-id="097f4-1802">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="097f4-1803">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="097f4-1804">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-1806">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="097f4-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1807">Az.Compute</span></span>
* <span data-ttu-id="097f4-1808">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="097f4-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="097f4-1809">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="097f4-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="097f4-1810">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="097f4-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="097f4-1811">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="097f4-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1813">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="097f4-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="097f4-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1814">Az.EventHub</span></span>
* <span data-ttu-id="097f4-1815">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="097f4-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1816">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-1817">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="097f4-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="097f4-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1818">Az.LogicApp</span></span>
* <span data-ttu-id="097f4-1819">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="097f4-1820">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="097f4-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="097f4-1821">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="097f4-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="097f4-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="097f4-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="097f4-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="097f4-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="097f4-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="097f4-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="097f4-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="097f4-1826">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="097f4-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="097f4-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="097f4-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="097f4-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="097f4-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="097f4-1831">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="097f4-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="097f4-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-1832">Az.Monitor</span></span>
* <span data-ttu-id="097f4-1833">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="097f4-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1834">Az.Network</span></span>
* <span data-ttu-id="097f4-1835">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="097f4-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="097f4-1837">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="097f4-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="097f4-1838">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="097f4-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="097f4-1839">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="097f4-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1840">Az.Resources</span></span>
* <span data-ttu-id="097f4-1841">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="097f4-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="097f4-1842">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="097f4-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="097f4-1843">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="097f4-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="097f4-1844">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="097f4-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1845">Az.Sql</span></span>
* <span data-ttu-id="097f4-1846">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="097f4-1847">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="097f4-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1848">Az.Websites</span></span>
* <span data-ttu-id="097f4-1849">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="097f4-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="097f4-1850">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1851">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1852">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="097f4-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="097f4-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="097f4-1854">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="097f4-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1855">Az.Compute</span></span>
* <span data-ttu-id="097f4-1856">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="097f4-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="097f4-1857">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="097f4-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="097f4-1858">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="097f4-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="097f4-1860">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="097f4-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1861">Az.Resources</span></span>
* <span data-ttu-id="097f4-1862">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="097f4-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="097f4-1863">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="097f4-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="097f4-1864">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="097f4-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="097f4-1865">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="097f4-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1866">Az.Sql</span></span>
* <span data-ttu-id="097f4-1867">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="097f4-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="097f4-1868">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="097f4-1869">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="097f4-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="097f4-1870">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1871">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1872">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="097f4-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="097f4-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="097f4-1874">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="097f4-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="097f4-1876">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="097f4-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="097f4-1877">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1878">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1879">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="097f4-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="097f4-1880">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="097f4-1881">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="097f4-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="097f4-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="097f4-1882">Az.Aks</span></span>
* <span data-ttu-id="097f4-1883">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="097f4-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-1884">Az.Automation</span></span>
* <span data-ttu-id="097f4-1885">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="097f4-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="097f4-1886">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="097f4-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="097f4-1887">Az.Cdn</span></span>
* <span data-ttu-id="097f4-1888">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1889">Az.Compute</span></span>
* <span data-ttu-id="097f4-1890">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="097f4-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="097f4-1891">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="097f4-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="097f4-1892">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="097f4-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="097f4-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="097f4-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="097f4-1894">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="097f4-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="097f4-1895">Az.DataFactory</span></span>
* <span data-ttu-id="097f4-1896">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="097f4-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1898">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="097f4-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="097f4-1899">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="097f4-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="097f4-1900">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1901">Az.IotHub</span></span>
* <span data-ttu-id="097f4-1902">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="097f4-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="097f4-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-1903">Az.KeyVault</span></span>
* <span data-ttu-id="097f4-1904">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-1905">Az.Network</span></span>
* <span data-ttu-id="097f4-1906">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1907">Az.Resources</span></span>
* <span data-ttu-id="097f4-1908">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="097f4-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="097f4-1909">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="097f4-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="097f4-1910">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="097f4-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="097f4-1911">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="097f4-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="097f4-1912">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="097f4-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="097f4-1913">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="097f4-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="097f4-1914">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="097f4-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-1916">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="097f4-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="097f4-1917">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="097f4-1917">Fix some error messages.</span></span>
* <span data-ttu-id="097f4-1918">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="097f4-1919">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="097f4-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="097f4-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="097f4-1920">Az.SignalR</span></span>
* <span data-ttu-id="097f4-1921">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1922">Az.Sql</span></span>
* <span data-ttu-id="097f4-1923">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="097f4-1924">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="097f4-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="097f4-1925">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="097f4-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="097f4-1926">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="097f4-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1927">Az.Storage</span></span>
* <span data-ttu-id="097f4-1928">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="097f4-1929">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="097f4-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="097f4-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="097f4-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="097f4-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="097f4-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="097f4-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="097f4-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="097f4-1933">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1934">Az.Websites</span></span>
* <span data-ttu-id="097f4-1935">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="097f4-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="097f4-1936">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="097f4-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="097f4-1937">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="097f4-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="097f4-1938">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="097f4-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1939">Az.Accounts</span></span>
* <span data-ttu-id="097f4-1940">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="097f4-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-1941">Az.Compute</span></span>
* <span data-ttu-id="097f4-1942">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="097f4-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="097f4-1943">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="097f4-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="097f4-1944">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-1946">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="097f4-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="097f4-1947">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="097f4-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="097f4-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="097f4-1948">Az.EventGrid</span></span>
* <span data-ttu-id="097f4-1949">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="097f4-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="097f4-1950">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="097f4-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="097f4-1951">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="097f4-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="097f4-1952">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="097f4-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="097f4-1953">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="097f4-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="097f4-1954">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="097f4-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="097f4-1955">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="097f4-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="097f4-1956">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="097f4-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="097f4-1957">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="097f4-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="097f4-1958">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="097f4-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="097f4-1959">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="097f4-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="097f4-1960">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="097f4-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="097f4-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1961">Az.IotHub</span></span>
* <span data-ttu-id="097f4-1962">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="097f4-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="097f4-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="097f4-1963">Az.LogicApp</span></span>
* <span data-ttu-id="097f4-1964">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="097f4-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-1965">Az.Resources</span></span>
* <span data-ttu-id="097f4-1966">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="097f4-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="097f4-1967">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="097f4-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="097f4-1968">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="097f4-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="097f4-1969">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="097f4-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="097f4-1970">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="097f4-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="097f4-1971">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="097f4-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="097f4-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="097f4-1972">Az.SignalR</span></span>
* <span data-ttu-id="097f4-1973">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-1974">Az.Sql</span></span>
* <span data-ttu-id="097f4-1975">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="097f4-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="097f4-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-1976">Az.Storage</span></span>
* <span data-ttu-id="097f4-1977">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="097f4-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="097f4-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="097f4-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="097f4-1979">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="097f4-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="097f4-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="097f4-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-1981">Az.Websites</span></span>
* <span data-ttu-id="097f4-1982">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="097f4-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="097f4-1983">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="097f4-1984">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="097f4-1985">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-1985">General</span></span>

- <span data-ttu-id="097f4-1986">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="097f4-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="097f4-1987">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="097f4-1987">Online help for each module</span></span>
- <span data-ttu-id="097f4-1988">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="097f4-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="097f4-1989">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="097f4-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="097f4-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-1990">Az.Accounts</span></span>
- <span data-ttu-id="097f4-1991">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="097f4-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="097f4-1992">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="097f4-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="097f4-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="097f4-1994">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="097f4-1994">Fixes for #7002</span></span>
- <span data-ttu-id="097f4-1995">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="097f4-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="097f4-1996">Az.Batch</span></span>
- <span data-ttu-id="097f4-1997">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="097f4-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="097f4-1998">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="097f4-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="097f4-1999">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="097f4-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="097f4-2000">Az.Billing</span></span>
- <span data-ttu-id="097f4-2001">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="097f4-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="097f4-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="097f4-2003">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="097f4-2004">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="097f4-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="097f4-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="097f4-2006">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="097f4-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="097f4-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="097f4-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="097f4-2008">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="097f4-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="097f4-2010">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="097f4-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="097f4-2011">Az.Monitor</span></span>
- <span data-ttu-id="097f4-2012">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="097f4-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="097f4-2013">Az.KeyVault</span></span>
- <span data-ttu-id="097f4-2014">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="097f4-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="097f4-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="097f4-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="097f4-2016">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="097f4-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="097f4-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="097f4-2017">Az.Media</span></span>
- <span data-ttu-id="097f4-2018">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="097f4-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="097f4-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-2019">Az.Network</span></span>
<span data-ttu-id="097f4-2020">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="097f4-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="097f4-2021">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="097f4-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="097f4-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="097f4-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="097f4-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="097f4-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="097f4-2030">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="097f4-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="097f4-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="097f4-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="097f4-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="097f4-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="097f4-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="097f4-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="097f4-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="097f4-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="097f4-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="097f4-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="097f4-2037">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="097f4-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="097f4-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="097f4-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="097f4-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="097f4-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="097f4-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="097f4-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="097f4-2041">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="097f4-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="097f4-2042">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="097f4-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="097f4-2044">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="097f4-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="097f4-2045">Az.Profile</span></span>
- <span data-ttu-id="097f4-2046">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="097f4-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="097f4-2048">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="097f4-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2049">Az.Resources</span></span>
- <span data-ttu-id="097f4-2050">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="097f4-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="097f4-2052">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="097f4-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="097f4-2053">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="097f4-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="097f4-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="097f4-2055">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="097f4-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="097f4-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-2056">Az.Sql</span></span>
- <span data-ttu-id="097f4-2057">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="097f4-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="097f4-2058">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="097f4-2059">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="097f4-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-2060">Az.Storage</span></span>
- <span data-ttu-id="097f4-2061">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="097f4-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-2062">Az.Websites</span></span>
- <span data-ttu-id="097f4-2063">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="097f4-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="097f4-2064">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="097f4-2065">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-2065">General</span></span>

* <span data-ttu-id="097f4-2066">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="097f4-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="097f4-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-2067">Az.Compute</span></span>

* <span data-ttu-id="097f4-2068">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="097f4-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="097f4-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="097f4-2070">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="097f4-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="097f4-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="097f4-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="097f4-2072">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="097f4-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="097f4-2073">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="097f4-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="097f4-2074">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="097f4-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="097f4-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="097f4-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="097f4-2076">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="097f4-2077">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="097f4-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="097f4-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2078">Az.Resources</span></span>

* <span data-ttu-id="097f4-2079">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="097f4-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="097f4-2080">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="097f4-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="097f4-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-2081">Az.Sql</span></span>

* <span data-ttu-id="097f4-2082">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="097f4-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="097f4-2083">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="097f4-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="097f4-2084">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="097f4-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="097f4-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-2085">Az.Storage</span></span>

* <span data-ttu-id="097f4-2086">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="097f4-2087">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="097f4-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="097f4-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="097f4-2089">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="097f4-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="097f4-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="097f4-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="097f4-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="097f4-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="097f4-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-2092">Az.Websites</span></span>

* <span data-ttu-id="097f4-2093">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="097f4-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="097f4-2094">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="097f4-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="097f4-2095">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="097f4-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="097f4-2096">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="097f4-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="097f4-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="097f4-2098">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="097f4-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="097f4-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="097f4-2099">Az.Automation</span></span>
* <span data-ttu-id="097f4-2100">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="097f4-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="097f4-2101">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="097f4-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="097f4-2102">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="097f4-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="097f4-2103">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="097f4-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="097f4-2104">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="097f4-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="097f4-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-2105">Az.Compute</span></span>
* <span data-ttu-id="097f4-2106">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="097f4-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="097f4-2107">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="097f4-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="097f4-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="097f4-2109">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="097f4-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="097f4-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="097f4-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="097f4-2111">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="097f4-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="097f4-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-2112">Az.Network</span></span>
* <span data-ttu-id="097f4-2113">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="097f4-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="097f4-2114">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="097f4-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="097f4-2115">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="097f4-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="097f4-2116">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="097f4-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="097f4-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="097f4-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="097f4-2118">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="097f4-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="097f4-2119">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="097f4-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="097f4-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="097f4-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="097f4-2121">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="097f4-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="097f4-2122">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="097f4-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="097f4-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="097f4-2123">Az.Relay</span></span>
* <span data-ttu-id="097f4-2124">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="097f4-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="097f4-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2125">Az.Resources</span></span>
* <span data-ttu-id="097f4-2126">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="097f4-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="097f4-2127">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="097f4-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="097f4-2128">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="097f4-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="097f4-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-2130">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="097f4-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="097f4-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-2131">Az.Sql</span></span>
* <span data-ttu-id="097f4-2132">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="097f4-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="097f4-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="097f4-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="097f4-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="097f4-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="097f4-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="097f4-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="097f4-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="097f4-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="097f4-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="097f4-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="097f4-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="097f4-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="097f4-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="097f4-2141">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="097f4-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="097f4-2142">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="097f4-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="097f4-2143">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="097f4-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="097f4-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="097f4-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="097f4-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="097f4-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="097f4-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="097f4-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="097f4-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="097f4-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="097f4-2148">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="097f4-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="097f4-2149">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="097f4-2150">Ogólne</span><span class="sxs-lookup"><span data-stu-id="097f4-2150">General</span></span>
* <span data-ttu-id="097f4-2151">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="097f4-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="097f4-2152">Az.Profile</span></span>
* <span data-ttu-id="097f4-2153">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="097f4-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="097f4-2154">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="097f4-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="097f4-2155">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="097f4-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="097f4-2156">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="097f4-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="097f4-2157">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="097f4-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="097f4-2158">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="097f4-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="097f4-2159">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="097f4-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-2161">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="097f4-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-2162">Az.Compute</span></span>
* <span data-ttu-id="097f4-2163">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="097f4-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="097f4-2164">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="097f4-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="097f4-2165">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="097f4-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-2167">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="097f4-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="097f4-2168">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="097f4-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="097f4-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="097f4-2169">Az.Insights</span></span>
* <span data-ttu-id="097f4-2170">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="097f4-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="097f4-2171">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="097f4-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="097f4-2172">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="097f4-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="097f4-2173">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="097f4-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-2174">Az.Network</span></span>
* <span data-ttu-id="097f4-2175">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="097f4-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="097f4-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="097f4-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="097f4-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="097f4-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="097f4-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="097f4-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="097f4-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="097f4-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="097f4-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="097f4-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="097f4-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="097f4-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="097f4-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="097f4-2183">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="097f4-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2184">Az.Resources</span></span>
* <span data-ttu-id="097f4-2185">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="097f4-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="097f4-2186">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="097f4-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="097f4-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="097f4-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="097f4-2188">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="097f4-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="097f4-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="097f4-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="097f4-2190">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="097f4-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="097f4-2191">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="097f4-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="097f4-2192">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="097f4-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="097f4-2193">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="097f4-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="097f4-2194">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="097f4-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="097f4-2195">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="097f4-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="097f4-2196">Az.Profile</span></span>
* <span data-ttu-id="097f4-2197">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="097f4-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="097f4-2198">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="097f4-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-2199">Az.Compute</span></span>
* <span data-ttu-id="097f4-2200">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="097f4-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="097f4-2201">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="097f4-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="097f4-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="097f4-2203">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="097f4-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="097f4-2204">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="097f4-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="097f4-2205">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="097f4-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="097f4-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="097f4-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="097f4-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="097f4-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-2208">Az.Network</span></span>
* <span data-ttu-id="097f4-2209">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="097f4-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="097f4-2210">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097f4-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2211">Az.Resources</span></span>
* <span data-ttu-id="097f4-2212">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="097f4-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="097f4-2213">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="097f4-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="097f4-2214">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="097f4-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="097f4-2215">Azure.Storage</span></span>
* <span data-ttu-id="097f4-2216">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="097f4-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="097f4-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="097f4-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="097f4-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="097f4-2219">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="097f4-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="097f4-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="097f4-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="097f4-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="097f4-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="097f4-2222">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="097f4-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="097f4-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="097f4-2223">Az.Compute</span></span>
* <span data-ttu-id="097f4-2224">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="097f4-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="097f4-2225">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="097f4-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="097f4-2226">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="097f4-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="097f4-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="097f4-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="097f4-2228">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="097f4-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="097f4-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="097f4-2229">Az.Network</span></span>
* <span data-ttu-id="097f4-2230">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="097f4-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="097f4-2231">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="097f4-2231">new cmdlets added</span></span>
    - <span data-ttu-id="097f4-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="097f4-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="097f4-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="097f4-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="097f4-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="097f4-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="097f4-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="097f4-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="097f4-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="097f4-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="097f4-2238">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="097f4-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="097f4-2239">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="097f4-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="097f4-2240">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="097f4-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="097f4-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="097f4-2241">Az.RedisCache</span></span>
* <span data-ttu-id="097f4-2242">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="097f4-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="097f4-2243">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="097f4-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="097f4-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="097f4-2244">Az.Resources</span></span>
* <span data-ttu-id="097f4-2245">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="097f4-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="097f4-2246">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="097f4-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="097f4-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="097f4-2247">Az.Sql</span></span>
* <span data-ttu-id="097f4-2248">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="097f4-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="097f4-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="097f4-2249">Az.Websites</span></span>
* <span data-ttu-id="097f4-2250">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="097f4-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="097f4-2251">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="097f4-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="097f4-2252">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="097f4-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="097f4-2253">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="097f4-2253">Initial Release</span></span>
