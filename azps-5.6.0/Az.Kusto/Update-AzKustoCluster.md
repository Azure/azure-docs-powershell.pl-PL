---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 21a2869a7a8006fdc0a570ebf4176f28c3a44efc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980385"
---
# <span data-ttu-id="41e8c-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="41e8c-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="41e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="41e8c-103">Aktualizowanie klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="41e8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41e8c-104">SYNTAX</span></span>

### <span data-ttu-id="41e8c-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="41e8c-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41e8c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="41e8c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41e8c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="41e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="41e8c-108">Aktualizowanie klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="41e8c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="41e8c-110">Przykład 1. Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="41e8c-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="41e8c-111">Powyższe polecenie aktualizuje klaster Kusto "testnewkustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="41e8c-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="41e8c-112">Przykład 2. Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="41e8c-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="41e8c-113">Powyższe polecenie aktualizuje klaster "testnewkustocluster" znaleziony w grupie zasobów "testrg" przy użyciu klucza zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="41e8c-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="41e8c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41e8c-114">PARAMETERS</span></span>

### <span data-ttu-id="41e8c-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="41e8c-115">-AsJob</span></span>
<span data-ttu-id="41e8c-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="41e8c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="41e8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e8c-117">-DefaultProfile</span></span>
<span data-ttu-id="41e8c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41e8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e8c-119">-EnableCryption</span><span class="sxs-lookup"><span data-stu-id="41e8c-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="41e8c-120">Wartość logiczna wskazująca, czy dyskerowanie klastrów jest szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="41e8c-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="41e8c-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="41e8c-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="41e8c-122">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="41e8c-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="41e8c-123">- EnablePurge</span><span class="sxs-lookup"><span data-stu-id="41e8c-123">-EnablePurge</span></span>
<span data-ttu-id="41e8c-124">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="41e8c-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="41e8c-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="41e8c-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="41e8c-126">Wartość logiczna wskazująca, czy funkcja przesyłania strumieniowego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="41e8c-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="41e8c-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="41e8c-127">-EngineType</span></span>
<span data-ttu-id="41e8c-128">Typ aparatu</span><span class="sxs-lookup"><span data-stu-id="41e8c-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e8c-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="41e8c-129">-IdentityType</span></span>
<span data-ttu-id="41e8c-130">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="41e8c-130">The type of managed identity used.</span></span>
<span data-ttu-id="41e8c-131">Typ "SystemAssigned, UserAssigned" obejmuje zarówno tożsamość utworzoną niejawnie, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="41e8c-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="41e8c-132">Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="41e8c-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="41e8c-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="41e8c-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="41e8c-134">Lista tożsamości użytkowników skojarzonych z klastrem Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="41e8c-135">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="41e8c-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="41e8c-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41e8c-136">-InputObject</span></span>
<span data-ttu-id="41e8c-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="41e8c-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41e8c-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="41e8c-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="41e8c-139">Nazwa klucza magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="41e8c-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="41e8c-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="41e8c-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="41e8c-141">Uri magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="41e8c-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="41e8c-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="41e8c-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="41e8c-143">Wersja klucza magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="41e8c-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="41e8c-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="41e8c-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="41e8c-145">Użytkownikowi przypisano tożsamość (ARM identyfikator zasobu), która ma dostęp do klucza.</span><span class="sxs-lookup"><span data-stu-id="41e8c-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="41e8c-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="41e8c-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="41e8c-147">Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="41e8c-147">The list of language extensions.</span></span>
<span data-ttu-id="41e8c-148">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach LANGUAGEEXTENSIONVALUE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="41e8c-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e8c-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="41e8c-149">-Location</span></span>
<span data-ttu-id="41e8c-150">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="41e8c-150">Resource location.</span></span>

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

### <span data-ttu-id="41e8c-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41e8c-151">-Name</span></span>
<span data-ttu-id="41e8c-152">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="41e8c-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41e8c-153">-NoWait</span></span>
<span data-ttu-id="41e8c-154">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="41e8c-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41e8c-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="41e8c-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="41e8c-156">Wartość logiczna wskazująca, czy funkcja zoptymalizowanego skalowania automatycznego jest włączona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="41e8c-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="41e8c-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="41e8c-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="41e8c-158">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="41e8c-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="41e8c-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="41e8c-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="41e8c-160">Zliczane są minimalne dozwolone wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="41e8c-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="41e8c-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="41e8c-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="41e8c-162">Wersja zdefiniowanego szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="41e8c-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="41e8c-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e8c-163">-ResourceGroupName</span></span>
<span data-ttu-id="41e8c-164">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="41e8c-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="41e8c-165">-SkuCapacity</span></span>
<span data-ttu-id="41e8c-166">Liczba wystąpień klastrów.</span><span class="sxs-lookup"><span data-stu-id="41e8c-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="41e8c-167">-SKUName</span><span class="sxs-lookup"><span data-stu-id="41e8c-167">-SkuName</span></span>
<span data-ttu-id="41e8c-168">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="41e8c-168">SKU name.</span></span>

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

### <span data-ttu-id="41e8c-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="41e8c-169">-SkuTier</span></span>
<span data-ttu-id="41e8c-170">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="41e8c-170">SKU tier.</span></span>

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

### <span data-ttu-id="41e8c-171">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41e8c-171">-SubscriptionId</span></span>
<span data-ttu-id="41e8c-172">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41e8c-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41e8c-173">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="41e8c-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41e8c-174">— Tag</span><span class="sxs-lookup"><span data-stu-id="41e8c-174">-Tag</span></span>
<span data-ttu-id="41e8c-175">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="41e8c-175">Resource tags.</span></span>

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

### <span data-ttu-id="41e8c-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="41e8c-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="41e8c-177">Dzierżawy zewnętrzne klastrów.</span><span class="sxs-lookup"><span data-stu-id="41e8c-177">The cluster's external tenants.</span></span>
<span data-ttu-id="41e8c-178">Aby skonstruować, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach TRUSTEDEXTERNALTENANT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="41e8c-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e8c-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="41e8c-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="41e8c-180">Identyfikator publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="41e8c-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="41e8c-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="41e8c-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="41e8c-182">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="41e8c-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="41e8c-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="41e8c-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="41e8c-184">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="41e8c-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="41e8c-185">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41e8c-185">-Confirm</span></span>
<span data-ttu-id="41e8c-186">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41e8c-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e8c-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e8c-187">-WhatIf</span></span>
<span data-ttu-id="41e8c-188">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41e8c-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e8c-189">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41e8c-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e8c-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e8c-190">CommonParameters</span></span>
<span data-ttu-id="41e8c-191">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e8c-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e8c-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41e8c-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e8c-193">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41e8c-193">INPUTS</span></span>

### <span data-ttu-id="41e8c-194">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="41e8c-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="41e8c-195">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41e8c-195">OUTPUTS</span></span>

### <span data-ttu-id="41e8c-196">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="41e8c-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="41e8c-197">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41e8c-197">NOTES</span></span>

<span data-ttu-id="41e8c-198">ALIASY</span><span class="sxs-lookup"><span data-stu-id="41e8c-198">ALIASES</span></span>

<span data-ttu-id="41e8c-199">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41e8c-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41e8c-200">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="41e8c-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41e8c-201">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41e8c-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41e8c-202">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="41e8c-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41e8c-203">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="41e8c-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="41e8c-204">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="41e8c-205">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="41e8c-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="41e8c-206">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="41e8c-207">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="41e8c-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41e8c-208">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="41e8c-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="41e8c-209">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="41e8c-210">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41e8c-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="41e8c-211">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41e8c-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41e8c-212">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="41e8c-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="41e8c-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="41e8c-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="41e8c-214">`[Name <LanguageExtensionName?>]`: nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="41e8c-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="41e8c-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Dzierżawy zewnętrzne klastrów.</span><span class="sxs-lookup"><span data-stu-id="41e8c-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="41e8c-216">`[Value <String>]`: identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="41e8c-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="41e8c-217">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41e8c-217">RELATED LINKS</span></span>

