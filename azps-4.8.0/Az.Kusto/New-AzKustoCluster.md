---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222519"
---
# <span data-ttu-id="3079e-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3079e-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="3079e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3079e-102">SYNOPSIS</span></span>
<span data-ttu-id="3079e-103">Utwórz lub zaktualizuj klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3079e-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="3079e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3079e-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3079e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3079e-105">DESCRIPTION</span></span>
<span data-ttu-id="3079e-106">Utwórz lub zaktualizuj klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3079e-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="3079e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3079e-107">EXAMPLES</span></span>

### <span data-ttu-id="3079e-108">Przykład 1. Utwórz nowy klaster Kusto</span><span class="sxs-lookup"><span data-stu-id="3079e-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="3079e-109">Powyższe polecenie tworzy nowy klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="3079e-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="3079e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3079e-110">PARAMETERS</span></span>

### <span data-ttu-id="3079e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3079e-111">-AsJob</span></span>
<span data-ttu-id="3079e-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3079e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3079e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3079e-113">-DefaultProfile</span></span>
<span data-ttu-id="3079e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3079e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3079e-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3079e-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="3079e-116">Wartość logiczna wskazująca, czy dyski klastra są szyfrowane.</span><span class="sxs-lookup"><span data-stu-id="3079e-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="3079e-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="3079e-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="3079e-118">Wartość logiczna wskazująca, czy jest włączone podwójne szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="3079e-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="3079e-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="3079e-119">-EnablePurge</span></span>
<span data-ttu-id="3079e-120">Wartość logiczna wskazująca, czy operacje przeczyszczania są włączone.</span><span class="sxs-lookup"><span data-stu-id="3079e-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="3079e-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="3079e-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="3079e-122">Wartość logiczna wskazująca, czy jest włączone strumieniowe pokarmowanie.</span><span class="sxs-lookup"><span data-stu-id="3079e-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="3079e-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3079e-123">-IdentityType</span></span>
<span data-ttu-id="3079e-124">Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="3079e-124">The identity type.</span></span>

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

### <span data-ttu-id="3079e-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3079e-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="3079e-126">Lista tożsamości użytkowników skojarzonych z klastrem usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="3079e-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="3079e-127">Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="3079e-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="3079e-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="3079e-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="3079e-129">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3079e-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="3079e-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3079e-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="3079e-131">Identyfikator URI magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3079e-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="3079e-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3079e-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="3079e-133">Wersja klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3079e-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="3079e-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="3079e-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="3079e-135">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="3079e-135">The list of language extensions.</span></span>
<span data-ttu-id="3079e-136">Aby skonstruować, zobacz sekcję notatki dla właściwości LANGUAGEEXTENSIONVALUE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3079e-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3079e-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3079e-137">-Location</span></span>
<span data-ttu-id="3079e-138">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="3079e-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="3079e-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3079e-139">-Name</span></span>
<span data-ttu-id="3079e-140">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="3079e-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3079e-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3079e-141">-NoWait</span></span>
<span data-ttu-id="3079e-142">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3079e-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3079e-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="3079e-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="3079e-144">Wartość logiczna wskazująca, czy zoptymalizowana funkcja skalowania automatycznego jest włączona.</span><span class="sxs-lookup"><span data-stu-id="3079e-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="3079e-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="3079e-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="3079e-146">Maksymalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3079e-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="3079e-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="3079e-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="3079e-148">Minimalna dozwolona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3079e-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="3079e-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="3079e-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="3079e-150">Zdefiniowana wersja szablonu, na przykład 1.</span><span class="sxs-lookup"><span data-stu-id="3079e-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="3079e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3079e-151">-ResourceGroupName</span></span>
<span data-ttu-id="3079e-152">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3079e-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3079e-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3079e-153">-SkuCapacity</span></span>
<span data-ttu-id="3079e-154">Liczba wystąpień klastra.</span><span class="sxs-lookup"><span data-stu-id="3079e-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="3079e-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3079e-155">-SkuName</span></span>
<span data-ttu-id="3079e-156">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="3079e-156">SKU name.</span></span>

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

### <span data-ttu-id="3079e-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3079e-157">-SkuTier</span></span>
<span data-ttu-id="3079e-158">Warstwa SKU.</span><span class="sxs-lookup"><span data-stu-id="3079e-158">SKU tier.</span></span>

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

### <span data-ttu-id="3079e-159">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3079e-159">-SubscriptionId</span></span>
<span data-ttu-id="3079e-160">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3079e-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3079e-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3079e-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3079e-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="3079e-162">-Tag</span></span>
<span data-ttu-id="3079e-163">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3079e-163">Resource tags.</span></span>

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

### <span data-ttu-id="3079e-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="3079e-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="3079e-165">Dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="3079e-165">The cluster's external tenants.</span></span>
<span data-ttu-id="3079e-166">Aby skonstruować, zobacz sekcję notatki dla właściwości TRUSTEDEXTERNALTENANT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3079e-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3079e-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="3079e-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="3079e-168">Identyfikator zasobu publicznego adresu IP usługi zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="3079e-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="3079e-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="3079e-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="3079e-170">Identyfikator zasobu publicznego adresu IP usługi aparatu.</span><span class="sxs-lookup"><span data-stu-id="3079e-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="3079e-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="3079e-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="3079e-172">Identyfikator zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="3079e-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="3079e-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="3079e-173">-Zone</span></span>
<span data-ttu-id="3079e-174">Strefy dostępności klastra.</span><span class="sxs-lookup"><span data-stu-id="3079e-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="3079e-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3079e-175">-Confirm</span></span>
<span data-ttu-id="3079e-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3079e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3079e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3079e-177">-WhatIf</span></span>
<span data-ttu-id="3079e-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3079e-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3079e-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3079e-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3079e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3079e-180">CommonParameters</span></span>
<span data-ttu-id="3079e-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3079e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3079e-182">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3079e-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3079e-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3079e-183">INPUTS</span></span>

## <span data-ttu-id="3079e-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3079e-184">OUTPUTS</span></span>

### <span data-ttu-id="3079e-185">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="3079e-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="3079e-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3079e-186">NOTES</span></span>

<span data-ttu-id="3079e-187">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3079e-187">ALIASES</span></span>

<span data-ttu-id="3079e-188">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3079e-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3079e-189">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3079e-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3079e-190">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3079e-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3079e-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="3079e-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="3079e-192">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="3079e-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="3079e-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: dzierżawy zewnętrzne klastra.</span><span class="sxs-lookup"><span data-stu-id="3079e-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="3079e-194">`[Value <String>]`: Identyfikator GUID reprezentujący dzierżawę zewnętrzną.</span><span class="sxs-lookup"><span data-stu-id="3079e-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="3079e-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3079e-195">RELATED LINKS</span></span>

