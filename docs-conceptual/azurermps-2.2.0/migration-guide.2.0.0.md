# <a name="table-of-contents"></a><span data-ttu-id="e5909-101">Spis treści</span><span class="sxs-lookup"><span data-stu-id="e5909-101">Table of Contents</span></span>
1. [<span data-ttu-id="e5909-102">Usunięcie parametrów Force</span><span class="sxs-lookup"><span data-stu-id="e5909-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="e5909-103">Zmiana parametrów Tag</span><span class="sxs-lookup"><span data-stu-id="e5909-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="e5909-104">Istotne zmiany w poleceniach cmdlet usługi Storage</span><span class="sxs-lookup"><span data-stu-id="e5909-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="e5909-105">Istotne zmiany w poleceniach cmdlet usługi AD</span><span class="sxs-lookup"><span data-stu-id="e5909-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="e5909-106">Usunięcie parametrów Force</span><span class="sxs-lookup"><span data-stu-id="e5909-106">Removal of Force parameters</span></span>

<span data-ttu-id="e5909-107">W tej wersji usunęliśmy wszystkie przestarzałe parametry `Force` z poleceń cmdlet i powiązane ostrzeżenia o tym, że parametry zostaną usunięte w przyszłej wersji.</span><span class="sxs-lookup"><span data-stu-id="e5909-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="e5909-108">Zmiana ta dotyczy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e5909-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="e5909-109">**ApiManagement**</span><span class="sxs-lookup"><span data-stu-id="e5909-109">**ApiManagement**</span></span>
- <span data-ttu-id="e5909-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5909-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="e5909-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e5909-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="e5909-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e5909-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="e5909-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e5909-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="e5909-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e5909-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="e5909-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5909-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="e5909-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e5909-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="e5909-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e5909-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="e5909-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e5909-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="e5909-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e5909-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="e5909-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5909-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="e5909-121">**Automatyzacja**</span><span class="sxs-lookup"><span data-stu-id="e5909-121">**Automation**</span></span>
- <span data-ttu-id="e5909-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5909-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="e5909-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5909-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="e5909-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e5909-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="e5909-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e5909-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="e5909-126">**Batch**</span><span class="sxs-lookup"><span data-stu-id="e5909-126">**Batch**</span></span>
- <span data-ttu-id="e5909-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e5909-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="e5909-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e5909-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="e5909-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e5909-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="e5909-130">**DataFactories**</span><span class="sxs-lookup"><span data-stu-id="e5909-130">**DataFactories**</span></span>
- <span data-ttu-id="e5909-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5909-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="e5909-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e5909-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="e5909-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5909-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="e5909-134">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="e5909-134">**DataLakeStore**</span></span>
- <span data-ttu-id="e5909-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e5909-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="e5909-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e5909-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="e5909-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e5909-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="e5909-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="e5909-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="e5909-139">**OperationalInsights**</span><span class="sxs-lookup"><span data-stu-id="e5909-139">**OperationalInsights**</span></span>
- <span data-ttu-id="e5909-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e5909-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="e5909-141">**Profil**</span><span class="sxs-lookup"><span data-stu-id="e5909-141">**Profile**</span></span>
- <span data-ttu-id="e5909-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5909-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="e5909-143">**RedisCache**</span><span class="sxs-lookup"><span data-stu-id="e5909-143">**RedisCache**</span></span>
- <span data-ttu-id="e5909-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e5909-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="e5909-145">**Zasoby**</span><span class="sxs-lookup"><span data-stu-id="e5909-145">**Resources**</span></span>
- <span data-ttu-id="e5909-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e5909-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="e5909-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e5909-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="e5909-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5909-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="e5909-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5909-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="e5909-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5909-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="e5909-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e5909-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="e5909-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5909-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="e5909-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e5909-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="e5909-154">**Storage**</span><span class="sxs-lookup"><span data-stu-id="e5909-154">**Storage**</span></span>
- <span data-ttu-id="e5909-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5909-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="e5909-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5909-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="e5909-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5909-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="e5909-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5909-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="e5909-159">**StreamAnalytics**</span><span class="sxs-lookup"><span data-stu-id="e5909-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="e5909-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e5909-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="e5909-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="e5909-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="e5909-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e5909-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="e5909-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e5909-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="e5909-164">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e5909-164">**Tag**</span></span>
- <span data-ttu-id="e5909-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="e5909-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="e5909-166">Jeśli masz skrypt, który wykorzystuje dowolne z powyższych poleceń cmdlet, istotną zmianę można naprawić przez usunięcie parametru `Force`.</span><span class="sxs-lookup"><span data-stu-id="e5909-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="e5909-167">Zmiana parametrów Tag</span><span class="sxs-lookup"><span data-stu-id="e5909-167">Change of Tag parameters</span></span>

<span data-ttu-id="e5909-168">W tej wersji nazwa parametru `Tags` została zmieniona na `Tag`, a typ został zmieniony z `Hashtable[]` na `Hashtable`, co zmienia format par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="e5909-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="e5909-169">Wcześniej każdy wpis w elemencie `Hashtable[]` reprezentował pojedyncze parowanie klucz-wartość:</span><span class="sxs-lookup"><span data-stu-id="e5909-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="e5909-170">Teraz parametry `Name` i `Value` nie są już wymagane, co umożliwia tworzenie par klucz wartość przez przypisanie `Key = "Value"` w elemencie `Hashtable`:</span><span class="sxs-lookup"><span data-stu-id="e5909-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="e5909-171">Zmiana ta dotyczy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e5909-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="e5909-172">**Batch**</span><span class="sxs-lookup"><span data-stu-id="e5909-172">**Batch**</span></span>
- <span data-ttu-id="e5909-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="e5909-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="e5909-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="e5909-176">**Obliczanie**</span><span class="sxs-lookup"><span data-stu-id="e5909-176">**Compute**</span></span>
- <span data-ttu-id="e5909-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e5909-177">New-AzureRmVM</span></span>
- <span data-ttu-id="e5909-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e5909-178">Update-AzureRmVM</span></span>

<span data-ttu-id="e5909-179">**DataLakeAnalytics**</span><span class="sxs-lookup"><span data-stu-id="e5909-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="e5909-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="e5909-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="e5909-182">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="e5909-182">**DataLakeStore**</span></span>
- <span data-ttu-id="e5909-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="e5909-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="e5909-185">**Dns**</span><span class="sxs-lookup"><span data-stu-id="e5909-185">**Dns**</span></span>
- <span data-ttu-id="e5909-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5909-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="e5909-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e5909-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="e5909-188">**KeyVault**</span><span class="sxs-lookup"><span data-stu-id="e5909-188">**KeyVault**</span></span>
- <span data-ttu-id="e5909-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e5909-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="e5909-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e5909-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="e5909-191">**Sieć**</span><span class="sxs-lookup"><span data-stu-id="e5909-191">**Network**</span></span>
- <span data-ttu-id="e5909-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5909-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="e5909-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5909-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="e5909-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5909-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="e5909-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5909-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="e5909-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5909-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="e5909-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5909-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="e5909-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e5909-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="e5909-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5909-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="e5909-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5909-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="e5909-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5909-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="e5909-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e5909-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="e5909-203">New-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e5909-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="e5909-204">**Zasoby**</span><span class="sxs-lookup"><span data-stu-id="e5909-204">**Resources**</span></span>
- <span data-ttu-id="e5909-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5909-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="e5909-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5909-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="e5909-207">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5909-207">New-AzureRmResource</span></span>
- <span data-ttu-id="e5909-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5909-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="e5909-209">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5909-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="e5909-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5909-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="e5909-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="e5909-211">**SQL**</span></span>
- <span data-ttu-id="e5909-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e5909-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="e5909-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e5909-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="e5909-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e5909-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="e5909-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e5909-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="e5909-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e5909-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="e5909-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e5909-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="e5909-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e5909-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="e5909-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e5909-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="e5909-220">**Storage**</span><span class="sxs-lookup"><span data-stu-id="e5909-220">**Storage**</span></span>
- <span data-ttu-id="e5909-221">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="e5909-222">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5909-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="e5909-223">**TrafficManager**</span><span class="sxs-lookup"><span data-stu-id="e5909-223">**TrafficManager**</span></span>
- <span data-ttu-id="e5909-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5909-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="e5909-225">Jeśli masz skrypt, który wykorzystuje dowolne z powyższych poleceń cmdlet, istotną zmianę można naprawić, zmieniając parametr `Tags` na `Tag`, jak również zmieniając element `Tag` na nowy format.</span><span class="sxs-lookup"><span data-stu-id="e5909-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="e5909-226">Istotne zmiany w poleceniach cmdlet usługi Storage</span><span class="sxs-lookup"><span data-stu-id="e5909-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="e5909-227">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="e5909-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="e5909-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="e5909-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="e5909-229">Polecenie cmdlet zwraca teraz listę kluczy, a nie obiekt z właściwościami dla każdego klucza</span><span class="sxs-lookup"><span data-stu-id="e5909-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="e5909-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="e5909-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="e5909-231">Nazwa pola `StorageAccountRegenerateKeyResponse` w danych wyjściowych tego polecenia cmdlet została zmieniona na `StorageAccountListKeysResults` i teraz jest to lista kluczy, a nie obiekt z właściwościami dla każdego klucza</span><span class="sxs-lookup"><span data-stu-id="e5909-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="e5909-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="e5909-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="e5909-233">Nazwa pola `AccountType` w danych wyjściowych tego polecenia cmdlet została zmieniona na `Sku.Name`</span><span class="sxs-lookup"><span data-stu-id="e5909-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="e5909-234">Typ wyjściowy dla obiektu blob/tabeli/kolejki/pliku głównych punktów końcowych/pomocniczych obiektów końcowych zmienił się z `Uri` na `String`</span><span class="sxs-lookup"><span data-stu-id="e5909-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="e5909-235">Istotne zmiany w poleceniach cmdlet usługi AD</span><span class="sxs-lookup"><span data-stu-id="e5909-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="e5909-236">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="e5909-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="e5909-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="e5909-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="e5909-238">Nazwa pola `ServicePrincipalName` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ServicePrincipalNames` i obecnie to pole jest kolekcją.</span><span class="sxs-lookup"><span data-stu-id="e5909-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="e5909-239">Teraz wyświetla ono również nazwę `ApplicationId` jako jedną z głównych nazw usługi wraz z parametrem identifierUri.</span><span class="sxs-lookup"><span data-stu-id="e5909-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="e5909-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="e5909-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="e5909-241">Nazwa parametru `ApplicationObjectId` została zmieniona na `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="e5909-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="e5909-242">Nazwa elementu `ApplicationObjectId` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="e5909-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="e5909-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="e5909-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="e5909-244">Nazwa parametru `ApplicationObjectId` została zmieniona na `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="e5909-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="e5909-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="e5909-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="e5909-246">Nazwa elementu `ApplicationObjectId` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="e5909-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="e5909-247">Parametry `KeyValue`, `KeyUsage`, `KeyType` zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="e5909-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="e5909-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="e5909-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="e5909-249">Usunięto pole `Mail` z danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e5909-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="e5909-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="e5909-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="e5909-251">Usunięto pole `Mail` z danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e5909-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="e5909-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="e5909-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="e5909-253">Usunięto parametr `DisableAccount`.</span><span class="sxs-lookup"><span data-stu-id="e5909-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```