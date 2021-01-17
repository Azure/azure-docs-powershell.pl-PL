---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386281"
---
# <span data-ttu-id="16b00-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="16b00-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="16b00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16b00-102">SYNOPSIS</span></span>
<span data-ttu-id="16b00-103">Aktualizowanie klastra programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="16b00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16b00-104">SYNTAX</span></span>

### <span data-ttu-id="16b00-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16b00-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="16b00-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16b00-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="16b00-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16b00-107">DESCRIPTION</span></span>
<span data-ttu-id="16b00-108">Aktualizowanie klastra programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="16b00-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16b00-109">EXAMPLES</span></span>

### <span data-ttu-id="16b00-110">Przykład 1: Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="16b00-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="16b00-111">Powyższe polecenie aktualizuje jednostkę SKU klastra Kusto "testnewkustocluster" odnalezioną w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="16b00-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="16b00-112">Przykład 2: Aktualizowanie istniejącego klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="16b00-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="16b00-113">Powyższe polecenie aktualizuje klaster "testnewkustocluster" znajdujący się w grupie zasobów "testrg" z kluczem zarządzanym przez klienta.</span><span class="sxs-lookup"><span data-stu-id="16b00-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="16b00-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16b00-114">PARAMETERS</span></span>

### <span data-ttu-id="16b00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16b00-115">-AsJob</span></span>
<span data-ttu-id="16b00-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="16b00-116">Run the command as a job</span></span>

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

### <span data-ttu-id="16b00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b00-117">-DefaultProfile</span></span>
<span data-ttu-id="16b00-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16b00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b00-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="16b00-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="16b00-120">Wartość logiczna wskazująca, czy dyski klastra są szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="16b00-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="16b00-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="16b00-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="16b00-122">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="16b00-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="16b00-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="16b00-123">-EnablePurge</span></span>
<span data-ttu-id="16b00-124">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="16b00-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="16b00-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="16b00-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="16b00-126">Wartość logiczna wskazująca, czy jest włączone strumieniowe pokarmowanie.</span><span class="sxs-lookup"><span data-stu-id="16b00-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="16b00-127">-Engine</span><span class="sxs-lookup"><span data-stu-id="16b00-127">-EngineType</span></span>
<span data-ttu-id="16b00-128">Typ silnika</span><span class="sxs-lookup"><span data-stu-id="16b00-128">The engine type</span></span>

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

### <span data-ttu-id="16b00-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="16b00-129">-IdentityType</span></span>
<span data-ttu-id="16b00-130">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="16b00-130">The type of managed identity used.</span></span>
<span data-ttu-id="16b00-131">Typ "SystemAssigned, UserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="16b00-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="16b00-132">Typ "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="16b00-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="16b00-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="16b00-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="16b00-134">Lista tożsamości użytkowników skojarzonych z klastrem usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="16b00-135">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="16b00-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="16b00-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16b00-136">-InputObject</span></span>
<span data-ttu-id="16b00-137">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="16b00-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16b00-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="16b00-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="16b00-139">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="16b00-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="16b00-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="16b00-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="16b00-141">Identyfikator URI magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="16b00-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="16b00-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="16b00-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="16b00-143">Wersja klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="16b00-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="16b00-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="16b00-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="16b00-145">Tożsamość przypisana przez użytkownika (identyfikator zasobu ARM) z dostępem do klucza.</span><span class="sxs-lookup"><span data-stu-id="16b00-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="16b00-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="16b00-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="16b00-147">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="16b00-147">The list of language extensions.</span></span>
<span data-ttu-id="16b00-148">Aby skonstruować, zobacz sekcję notatki dla właściwości LANGUAGEEXTENSIONVALUE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="16b00-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="16b00-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="16b00-149">-Location</span></span>
<span data-ttu-id="16b00-150">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="16b00-150">Resource location.</span></span>

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

### <span data-ttu-id="16b00-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16b00-151">-Name</span></span>
<span data-ttu-id="16b00-152">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="16b00-153">-Nowait</span><span class="sxs-lookup"><span data-stu-id="16b00-153">-NoWait</span></span>
<span data-ttu-id="16b00-154">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="16b00-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="16b00-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="16b00-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="16b00-156">Wartość logiczna wskazująca, czy zoptymalizowana funkcja skalowania automatycznego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="16b00-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="16b00-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="16b00-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="16b00-158">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="16b00-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="16b00-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="16b00-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="16b00-160">Minimalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="16b00-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="16b00-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="16b00-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="16b00-162">Zdefiniowana wersja szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="16b00-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="16b00-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b00-163">-ResourceGroupName</span></span>
<span data-ttu-id="16b00-164">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="16b00-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="16b00-165">-SkuCapacity</span></span>
<span data-ttu-id="16b00-166">Liczba wystąpień klastra.</span><span class="sxs-lookup"><span data-stu-id="16b00-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="16b00-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="16b00-167">-SkuName</span></span>
<span data-ttu-id="16b00-168">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="16b00-168">SKU name.</span></span>

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

### <span data-ttu-id="16b00-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="16b00-169">-SkuTier</span></span>
<span data-ttu-id="16b00-170">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="16b00-170">SKU tier.</span></span>

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

### <span data-ttu-id="16b00-171">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="16b00-171">-SubscriptionId</span></span>
<span data-ttu-id="16b00-172">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16b00-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="16b00-173">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="16b00-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="16b00-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="16b00-174">-Tag</span></span>
<span data-ttu-id="16b00-175">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="16b00-175">Resource tags.</span></span>

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

### <span data-ttu-id="16b00-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="16b00-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="16b00-177">Dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="16b00-177">The cluster's external tenants.</span></span>
<span data-ttu-id="16b00-178">Aby skonstruować, zobacz sekcję notatki dla właściwości TRUSTEDEXTERNALTENANT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="16b00-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16b00-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="16b00-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="16b00-180">Identyfikator zasobu publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="16b00-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="16b00-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="16b00-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="16b00-182">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="16b00-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="16b00-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="16b00-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="16b00-184">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="16b00-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="16b00-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16b00-185">-Confirm</span></span>
<span data-ttu-id="16b00-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b00-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b00-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b00-187">-WhatIf</span></span>
<span data-ttu-id="16b00-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b00-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b00-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16b00-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b00-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b00-190">CommonParameters</span></span>
<span data-ttu-id="16b00-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b00-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b00-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16b00-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b00-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16b00-193">INPUTS</span></span>

### <span data-ttu-id="16b00-194">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="16b00-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="16b00-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16b00-195">OUTPUTS</span></span>

### <span data-ttu-id="16b00-196">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="16b00-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="16b00-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16b00-197">NOTES</span></span>

<span data-ttu-id="16b00-198">PISUJE</span><span class="sxs-lookup"><span data-stu-id="16b00-198">ALIASES</span></span>

<span data-ttu-id="16b00-199">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16b00-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16b00-200">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="16b00-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16b00-201">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16b00-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16b00-202">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="16b00-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16b00-203">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="16b00-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="16b00-204">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="16b00-205">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="16b00-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="16b00-206">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="16b00-207">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="16b00-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16b00-208">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16b00-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="16b00-209">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="16b00-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="16b00-210">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="16b00-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="16b00-211">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16b00-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="16b00-212">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="16b00-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="16b00-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="16b00-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="16b00-214">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="16b00-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="16b00-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="16b00-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="16b00-216">`[Value <String>]`: Identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="16b00-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="16b00-217">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16b00-217">RELATED LINKS</span></span>

