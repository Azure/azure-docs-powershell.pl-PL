---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501488"
---
# <span data-ttu-id="53751-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="53751-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="53751-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53751-102">SYNOPSIS</span></span>
<span data-ttu-id="53751-103">Utwórz lub zaktualizuj klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="53751-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="53751-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53751-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53751-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53751-105">DESCRIPTION</span></span>
<span data-ttu-id="53751-106">Utwórz lub zaktualizuj klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="53751-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="53751-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53751-107">EXAMPLES</span></span>

### <span data-ttu-id="53751-108">Przykład 1. Utwórz nowy klaster Kusto</span><span class="sxs-lookup"><span data-stu-id="53751-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="53751-109">Powyższe polecenie tworzy nowy klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="53751-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="53751-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53751-110">PARAMETERS</span></span>

### <span data-ttu-id="53751-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53751-111">-AsJob</span></span>
<span data-ttu-id="53751-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="53751-112">Run the command as a job</span></span>

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

### <span data-ttu-id="53751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53751-113">-DefaultProfile</span></span>
<span data-ttu-id="53751-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53751-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53751-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="53751-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="53751-116">Wartość logiczna wskazująca, czy dyski klastra są szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="53751-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="53751-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="53751-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="53751-118">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="53751-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="53751-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="53751-119">-EnablePurge</span></span>
<span data-ttu-id="53751-120">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="53751-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="53751-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="53751-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="53751-122">Wartość logiczna wskazująca, czy jest włączone strumieniowe pokarmowanie.</span><span class="sxs-lookup"><span data-stu-id="53751-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="53751-123">-Engine</span><span class="sxs-lookup"><span data-stu-id="53751-123">-EngineType</span></span>
<span data-ttu-id="53751-124">Typ silnika</span><span class="sxs-lookup"><span data-stu-id="53751-124">The engine type</span></span>

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

### <span data-ttu-id="53751-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="53751-125">-IdentityType</span></span>
<span data-ttu-id="53751-126">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="53751-126">The type of managed identity used.</span></span>
<span data-ttu-id="53751-127">Typ "SystemAssigned, UserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="53751-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="53751-128">Typ "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="53751-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="53751-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="53751-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="53751-130">Lista tożsamości użytkowników skojarzonych z klastrem usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="53751-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="53751-131">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="53751-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="53751-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="53751-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="53751-133">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="53751-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="53751-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="53751-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="53751-135">Identyfikator URI magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="53751-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="53751-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="53751-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="53751-137">Wersja klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="53751-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="53751-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="53751-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="53751-139">Tożsamość przypisana przez użytkownika (identyfikator zasobu ARM) z dostępem do klucza.</span><span class="sxs-lookup"><span data-stu-id="53751-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="53751-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="53751-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="53751-141">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="53751-141">The list of language extensions.</span></span>
<span data-ttu-id="53751-142">Aby skonstruować, zobacz sekcję notatki dla właściwości LANGUAGEEXTENSIONVALUE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="53751-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="53751-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="53751-143">-Location</span></span>
<span data-ttu-id="53751-144">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="53751-144">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53751-145">-Name</span></span>
<span data-ttu-id="53751-146">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="53751-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="53751-147">-NoWait</span></span>
<span data-ttu-id="53751-148">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="53751-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53751-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="53751-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="53751-150">Wartość logiczna wskazująca, czy zoptymalizowana funkcja skalowania automatycznego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="53751-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="53751-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="53751-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="53751-152">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="53751-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="53751-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="53751-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="53751-154">Minimalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="53751-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="53751-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="53751-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="53751-156">Zdefiniowana wersja szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="53751-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="53751-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53751-157">-ResourceGroupName</span></span>
<span data-ttu-id="53751-158">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="53751-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="53751-159">-SkuCapacity</span></span>
<span data-ttu-id="53751-160">Liczba wystąpień klastra.</span><span class="sxs-lookup"><span data-stu-id="53751-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="53751-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="53751-161">-SkuName</span></span>
<span data-ttu-id="53751-162">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="53751-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="53751-163">-SkuTier</span></span>
<span data-ttu-id="53751-164">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="53751-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-165">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="53751-165">-SubscriptionId</span></span>
<span data-ttu-id="53751-166">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53751-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53751-167">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="53751-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="53751-168">-Tag</span></span>
<span data-ttu-id="53751-169">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="53751-169">Resource tags.</span></span>

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

### <span data-ttu-id="53751-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="53751-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="53751-171">Dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="53751-171">The cluster's external tenants.</span></span>
<span data-ttu-id="53751-172">Aby skonstruować, zobacz sekcję notatki dla właściwości TRUSTEDEXTERNALTENANT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="53751-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53751-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="53751-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="53751-174">Identyfikator zasobu publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="53751-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="53751-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="53751-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="53751-176">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="53751-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="53751-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="53751-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="53751-178">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="53751-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="53751-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="53751-179">-Zone</span></span>
<span data-ttu-id="53751-180">Strefy dostępności klastra.</span><span class="sxs-lookup"><span data-stu-id="53751-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53751-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53751-181">-Confirm</span></span>
<span data-ttu-id="53751-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53751-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53751-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53751-183">-WhatIf</span></span>
<span data-ttu-id="53751-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53751-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53751-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53751-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53751-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53751-186">CommonParameters</span></span>
<span data-ttu-id="53751-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53751-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53751-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53751-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53751-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53751-189">INPUTS</span></span>

## <span data-ttu-id="53751-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53751-190">OUTPUTS</span></span>

### <span data-ttu-id="53751-191">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="53751-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="53751-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53751-192">NOTES</span></span>

<span data-ttu-id="53751-193">PISUJE</span><span class="sxs-lookup"><span data-stu-id="53751-193">ALIASES</span></span>

<span data-ttu-id="53751-194">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53751-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53751-195">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="53751-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53751-196">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53751-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53751-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="53751-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="53751-198">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="53751-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="53751-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="53751-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="53751-200">`[Value <String>]`: Identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="53751-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="53751-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53751-201">RELATED LINKS</span></span>

