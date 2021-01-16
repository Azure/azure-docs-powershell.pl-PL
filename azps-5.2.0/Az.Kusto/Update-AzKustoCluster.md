---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366900"
---
# <span data-ttu-id="a7f17-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="a7f17-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="a7f17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7f17-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f17-103">Aktualizowanie klastra programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="a7f17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7f17-104">SYNTAX</span></span>

### <span data-ttu-id="a7f17-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a7f17-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7f17-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a7f17-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7f17-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a7f17-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f17-108">Aktualizowanie klastra programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="a7f17-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7f17-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f17-110">Przykład 1: Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="a7f17-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="a7f17-111">Powyższe polecenie aktualizuje jednostkę SKU klastra Kusto "testnewkustocluster" odnalezioną w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="a7f17-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a7f17-112">Przykład 2: Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="a7f17-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="a7f17-113">Powyższe polecenie aktualizuje klaster "testnewkustocluster" znajdujący się w grupie zasobów "testrg" z kluczem zarządzanym przez klienta.</span><span class="sxs-lookup"><span data-stu-id="a7f17-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="a7f17-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7f17-114">PARAMETERS</span></span>

### <span data-ttu-id="a7f17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f17-115">-AsJob</span></span>
<span data-ttu-id="a7f17-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a7f17-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f17-117">-DefaultProfile</span></span>
<span data-ttu-id="a7f17-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a7f17-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="a7f17-120">Wartość logiczna wskazująca, czy dyski klastra są szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="a7f17-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="a7f17-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="a7f17-122">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="a7f17-122">A boolean value that indicates if double encryption is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="a7f17-123">-EnablePurge</span></span>
<span data-ttu-id="a7f17-124">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="a7f17-124">A boolean value that indicates if the purge operations are enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="a7f17-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="a7f17-126">Wartość logiczna wskazująca, czy jest włączone strumieniowe pokarmowanie.</span><span class="sxs-lookup"><span data-stu-id="a7f17-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a7f17-127">-IdentityType</span></span>
<span data-ttu-id="a7f17-128">Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a7f17-128">The identity type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a7f17-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="a7f17-130">Lista tożsamości użytkowników skojarzonych z klastrem usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="a7f17-131">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="a7f17-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7f17-132">-InputObject</span></span>
<span data-ttu-id="a7f17-133">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a7f17-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="a7f17-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="a7f17-135">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7f17-135">The name of the key vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a7f17-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="a7f17-137">Identyfikator URI magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7f17-137">The Uri of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="a7f17-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="a7f17-139">Wersja klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7f17-139">The version of the key vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="a7f17-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="a7f17-141">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="a7f17-141">The list of language extensions.</span></span>
<span data-ttu-id="a7f17-142">Aby skonstruować, zobacz sekcję notatki dla właściwości LANGUAGEEXTENSIONVALUE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a7f17-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a7f17-143">-Location</span></span>
<span data-ttu-id="a7f17-144">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a7f17-144">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7f17-145">-Name</span></span>
<span data-ttu-id="a7f17-146">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a7f17-147">-NoWait</span></span>
<span data-ttu-id="a7f17-148">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a7f17-148">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="a7f17-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="a7f17-150">Wartość logiczna wskazująca, czy zoptymalizowana funkcja skalowania automatycznego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="a7f17-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="a7f17-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="a7f17-152">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="a7f17-152">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="a7f17-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="a7f17-154">Minimalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="a7f17-154">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="a7f17-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="a7f17-156">Zdefiniowana wersja szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="a7f17-156">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f17-157">-ResourceGroupName</span></span>
<span data-ttu-id="a7f17-158">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a7f17-159">-SkuCapacity</span></span>
<span data-ttu-id="a7f17-160">Liczba wystąpień klastra.</span><span class="sxs-lookup"><span data-stu-id="a7f17-160">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a7f17-161">-SkuName</span></span>
<span data-ttu-id="a7f17-162">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="a7f17-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a7f17-163">-SkuTier</span></span>
<span data-ttu-id="a7f17-164">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="a7f17-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-165">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a7f17-165">-SubscriptionId</span></span>
<span data-ttu-id="a7f17-166">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f17-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a7f17-167">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a7f17-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7f17-168">-Tag</span></span>
<span data-ttu-id="a7f17-169">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7f17-169">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="a7f17-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="a7f17-171">Dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="a7f17-171">The cluster's external tenants.</span></span>
<span data-ttu-id="a7f17-172">Aby skonstruować, zobacz sekcję notatki dla właściwości TRUSTEDEXTERNALTENANT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a7f17-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="a7f17-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="a7f17-174">Identyfikator zasobu publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="a7f17-174">Data management's service public IP address resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="a7f17-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="a7f17-176">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="a7f17-176">Engine service's public IP address resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="a7f17-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="a7f17-178">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="a7f17-178">The subnet resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7f17-179">-Confirm</span></span>
<span data-ttu-id="a7f17-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f17-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f17-181">-WhatIf</span></span>
<span data-ttu-id="a7f17-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f17-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f17-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7f17-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f17-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f17-184">CommonParameters</span></span>
<span data-ttu-id="a7f17-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f17-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f17-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7f17-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f17-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7f17-187">INPUTS</span></span>

### <span data-ttu-id="a7f17-188">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a7f17-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a7f17-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7f17-189">OUTPUTS</span></span>

### <span data-ttu-id="a7f17-190">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="a7f17-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="a7f17-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7f17-191">NOTES</span></span>

<span data-ttu-id="a7f17-192">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a7f17-192">ALIASES</span></span>

<span data-ttu-id="a7f17-193">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7f17-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7f17-194">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a7f17-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7f17-195">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7f17-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7f17-196">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a7f17-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7f17-197">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a7f17-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a7f17-198">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a7f17-199">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="a7f17-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a7f17-200">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a7f17-201">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a7f17-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7f17-202">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f17-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a7f17-203">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a7f17-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a7f17-204">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a7f17-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a7f17-205">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f17-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a7f17-206">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a7f17-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="a7f17-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="a7f17-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="a7f17-208">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="a7f17-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="a7f17-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="a7f17-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="a7f17-210">`[Value <String>]`: Identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="a7f17-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="a7f17-211">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7f17-211">RELATED LINKS</span></span>

