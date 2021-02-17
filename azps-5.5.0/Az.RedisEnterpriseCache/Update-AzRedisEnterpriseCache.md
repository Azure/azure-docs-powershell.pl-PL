---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191234"
---
# <span data-ttu-id="0232e-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="0232e-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="0232e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0232e-102">SYNOPSIS</span></span>
<span data-ttu-id="0232e-103">Aktualizacje istniejącego klastra RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="0232e-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="0232e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0232e-104">SYNTAX</span></span>

### <span data-ttu-id="0232e-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0232e-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0232e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0232e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0232e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0232e-107">DESCRIPTION</span></span>
<span data-ttu-id="0232e-108">Aktualizacje istniejącego klastra RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="0232e-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="0232e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0232e-109">EXAMPLES</span></span>

### <span data-ttu-id="0232e-110">Przykład 1. Aktualizacja pamięci podręcznej Redis Enterprise</span><span class="sxs-lookup"><span data-stu-id="0232e-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="0232e-111">To polecenie aktualizuje minimalną wersję TLS i dodaje tag do pamięci podręcznej Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="0232e-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="0232e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0232e-112">PARAMETERS</span></span>

### <span data-ttu-id="0232e-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0232e-113">-AsJob</span></span>
<span data-ttu-id="0232e-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0232e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0232e-115">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="0232e-115">-Capacity</span></span>
<span data-ttu-id="0232e-116">Rozmiar klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="0232e-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="0232e-117">Wartość domyślna to 2 lub 3 w zależności od typu SKU.</span><span class="sxs-lookup"><span data-stu-id="0232e-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="0232e-118">Prawidłowe wartości to (2, 4, 6, ...) dla wersji Enterprise i (3, 9, 15, ...) dla wersji Flash.</span><span class="sxs-lookup"><span data-stu-id="0232e-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0232e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0232e-119">-ClusterName</span></span>
<span data-ttu-id="0232e-120">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="0232e-120">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0232e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0232e-121">-DefaultProfile</span></span>
<span data-ttu-id="0232e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0232e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0232e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0232e-123">-InputObject</span></span>
<span data-ttu-id="0232e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0232e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0232e-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0232e-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="0232e-126">Minimalna wersja TLS dla klastra do obsługi, na przykład "1,2"</span><span class="sxs-lookup"><span data-stu-id="0232e-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="0232e-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0232e-127">-NoWait</span></span>
<span data-ttu-id="0232e-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0232e-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0232e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0232e-129">-ResourceGroupName</span></span>
<span data-ttu-id="0232e-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0232e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0232e-131">- SKU</span><span class="sxs-lookup"><span data-stu-id="0232e-131">-Sku</span></span>
<span data-ttu-id="0232e-132">Typ klastrów RedisEnterprise do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0232e-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="0232e-133">Możliwe wartości: (Enterprise_E10, EnterpriseFlash_F300 itp.)</span><span class="sxs-lookup"><span data-stu-id="0232e-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0232e-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0232e-134">-SubscriptionId</span></span>
<span data-ttu-id="0232e-135">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0232e-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0232e-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0232e-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0232e-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="0232e-137">-Tag</span></span>
<span data-ttu-id="0232e-138">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="0232e-138">Resource tags.</span></span>

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

### <span data-ttu-id="0232e-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0232e-139">-Confirm</span></span>
<span data-ttu-id="0232e-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0232e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0232e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0232e-141">-WhatIf</span></span>
<span data-ttu-id="0232e-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0232e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0232e-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0232e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0232e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0232e-144">CommonParameters</span></span>
<span data-ttu-id="0232e-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0232e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0232e-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0232e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0232e-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0232e-147">INPUTS</span></span>

### <span data-ttu-id="0232e-148">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="0232e-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="0232e-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0232e-149">OUTPUTS</span></span>

### <span data-ttu-id="0232e-150">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="0232e-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="0232e-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0232e-151">NOTES</span></span>

<span data-ttu-id="0232e-152">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0232e-152">ALIASES</span></span>

<span data-ttu-id="0232e-153">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0232e-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0232e-154">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0232e-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0232e-155">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0232e-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0232e-156">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0232e-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0232e-157">`[ClusterName <String>]`: nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="0232e-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="0232e-158">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0232e-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0232e-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0232e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0232e-160">`[Location <String>]`: region, w który znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="0232e-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="0232e-161">`[OperationId <String>]`: czas trwania identyfikator unikatowy.</span><span class="sxs-lookup"><span data-stu-id="0232e-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="0232e-162">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0232e-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="0232e-163">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0232e-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0232e-164">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0232e-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0232e-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0232e-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0232e-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0232e-166">RELATED LINKS</span></span>

