---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959594"
---
# <span data-ttu-id="46249-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="46249-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="46249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46249-102">SYNOPSIS</span></span>
<span data-ttu-id="46249-103">Tworzenie lub aktualizowanie klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="46249-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="46249-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46249-104">SYNTAX</span></span>

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

## <span data-ttu-id="46249-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46249-105">DESCRIPTION</span></span>
<span data-ttu-id="46249-106">Tworzenie lub aktualizowanie klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="46249-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="46249-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46249-107">EXAMPLES</span></span>

### <span data-ttu-id="46249-108">Przykład 1. Tworzenie nowego klastru Kusto</span><span class="sxs-lookup"><span data-stu-id="46249-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="46249-109">Powyższe polecenie tworzy nowy klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="46249-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="46249-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46249-110">PARAMETERS</span></span>

### <span data-ttu-id="46249-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="46249-111">-AsJob</span></span>
<span data-ttu-id="46249-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="46249-112">Run the command as a job</span></span>

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

### <span data-ttu-id="46249-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46249-113">-DefaultProfile</span></span>
<span data-ttu-id="46249-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46249-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46249-115">-EnableCryption</span><span class="sxs-lookup"><span data-stu-id="46249-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="46249-116">Wartość logiczna wskazująca, czy dyskerowanie klastrów jest szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="46249-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="46249-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="46249-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="46249-118">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="46249-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="46249-119">- EnablePurge</span><span class="sxs-lookup"><span data-stu-id="46249-119">-EnablePurge</span></span>
<span data-ttu-id="46249-120">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="46249-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="46249-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="46249-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="46249-122">Wartość logiczna wskazująca, czy funkcja przesyłania strumieniowego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="46249-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="46249-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="46249-123">-EngineType</span></span>
<span data-ttu-id="46249-124">Typ aparatu</span><span class="sxs-lookup"><span data-stu-id="46249-124">The engine type</span></span>

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

### <span data-ttu-id="46249-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="46249-125">-IdentityType</span></span>
<span data-ttu-id="46249-126">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="46249-126">The type of managed identity used.</span></span>
<span data-ttu-id="46249-127">Typ "SystemAssigned, UserAssigned" obejmuje zarówno tożsamość utworzoną niejawnie, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="46249-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="46249-128">Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="46249-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="46249-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="46249-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="46249-130">Lista tożsamości użytkowników skojarzonych z klastrem Kusto.</span><span class="sxs-lookup"><span data-stu-id="46249-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="46249-131">Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="46249-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="46249-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="46249-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="46249-133">Nazwa klucza magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="46249-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="46249-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="46249-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="46249-135">Uri magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="46249-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="46249-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="46249-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="46249-137">Wersja klucza magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="46249-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="46249-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="46249-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="46249-139">Użytkownikowi przypisano tożsamość (ARM identyfikator zasobu), która ma dostęp do klucza.</span><span class="sxs-lookup"><span data-stu-id="46249-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="46249-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="46249-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="46249-141">Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="46249-141">The list of language extensions.</span></span>
<span data-ttu-id="46249-142">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach LANGUAGEEXTENSIONVALUE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="46249-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="46249-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46249-143">-Location</span></span>
<span data-ttu-id="46249-144">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="46249-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="46249-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="46249-145">-Name</span></span>
<span data-ttu-id="46249-146">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="46249-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="46249-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46249-147">-NoWait</span></span>
<span data-ttu-id="46249-148">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="46249-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46249-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="46249-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="46249-150">Wartość logiczna wskazująca, czy funkcja zoptymalizowanego skalowania automatycznego jest włączona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="46249-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="46249-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="46249-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="46249-152">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="46249-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="46249-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="46249-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="46249-154">Zliczane są minimalne dozwolone wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="46249-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="46249-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="46249-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="46249-156">Wersja zdefiniowanego szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="46249-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="46249-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46249-157">-ResourceGroupName</span></span>
<span data-ttu-id="46249-158">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="46249-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="46249-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="46249-159">-SkuCapacity</span></span>
<span data-ttu-id="46249-160">Liczba wystąpień klastrów.</span><span class="sxs-lookup"><span data-stu-id="46249-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="46249-161">-SKUName</span><span class="sxs-lookup"><span data-stu-id="46249-161">-SkuName</span></span>
<span data-ttu-id="46249-162">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="46249-162">SKU name.</span></span>

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

### <span data-ttu-id="46249-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="46249-163">-SkuTier</span></span>
<span data-ttu-id="46249-164">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="46249-164">SKU tier.</span></span>

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

### <span data-ttu-id="46249-165">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46249-165">-SubscriptionId</span></span>
<span data-ttu-id="46249-166">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46249-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46249-167">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="46249-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46249-168">— Tag</span><span class="sxs-lookup"><span data-stu-id="46249-168">-Tag</span></span>
<span data-ttu-id="46249-169">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="46249-169">Resource tags.</span></span>

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

### <span data-ttu-id="46249-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="46249-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="46249-171">Dzierżawy zewnętrzne klastrów.</span><span class="sxs-lookup"><span data-stu-id="46249-171">The cluster's external tenants.</span></span>
<span data-ttu-id="46249-172">Aby skonstruować, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach TRUSTEDEXTERNALTENANT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="46249-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46249-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="46249-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="46249-174">Identyfikator publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="46249-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="46249-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="46249-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="46249-176">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="46249-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="46249-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="46249-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="46249-178">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="46249-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="46249-179">— Strefa</span><span class="sxs-lookup"><span data-stu-id="46249-179">-Zone</span></span>
<span data-ttu-id="46249-180">Strefy dostępności klastrów.</span><span class="sxs-lookup"><span data-stu-id="46249-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="46249-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46249-181">-Confirm</span></span>
<span data-ttu-id="46249-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46249-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46249-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46249-183">-WhatIf</span></span>
<span data-ttu-id="46249-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46249-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46249-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="46249-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46249-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46249-186">CommonParameters</span></span>
<span data-ttu-id="46249-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46249-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46249-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46249-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46249-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46249-189">INPUTS</span></span>

## <span data-ttu-id="46249-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46249-190">OUTPUTS</span></span>

### <span data-ttu-id="46249-191">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="46249-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="46249-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46249-192">NOTES</span></span>

<span data-ttu-id="46249-193">ALIASY</span><span class="sxs-lookup"><span data-stu-id="46249-193">ALIASES</span></span>

<span data-ttu-id="46249-194">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46249-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46249-195">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="46249-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46249-196">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46249-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46249-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="46249-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="46249-198">`[Name <LanguageExtensionName?>]`: nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="46249-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="46249-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: Dzierżawy zewnętrzne klastrów.</span><span class="sxs-lookup"><span data-stu-id="46249-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="46249-200">`[Value <String>]`: identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="46249-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="46249-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46249-201">RELATED LINKS</span></span>

