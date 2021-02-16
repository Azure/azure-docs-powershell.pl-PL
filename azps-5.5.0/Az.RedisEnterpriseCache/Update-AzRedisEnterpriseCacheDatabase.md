---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201947"
---
# <span data-ttu-id="d5116-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="d5116-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="d5116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5116-102">SYNOPSIS</span></span>
<span data-ttu-id="d5116-103">Aktualizacje bazy danych</span><span class="sxs-lookup"><span data-stu-id="d5116-103">Updates a database</span></span>

## <span data-ttu-id="d5116-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5116-104">SYNTAX</span></span>

### <span data-ttu-id="d5116-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d5116-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5116-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5116-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d5116-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5116-107">DESCRIPTION</span></span>
<span data-ttu-id="d5116-108">Aktualizacje bazy danych</span><span class="sxs-lookup"><span data-stu-id="d5116-108">Updates a database</span></span>

## <span data-ttu-id="d5116-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5116-109">EXAMPLES</span></span>

### <span data-ttu-id="d5116-110">Przykład 1. Aktualizowanie protokołu klienta</span><span class="sxs-lookup"><span data-stu-id="d5116-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="d5116-111">To polecenie aktualizuje protokół klienta bazy danych dla funkcji Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="d5116-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="d5116-112">Przykład 2. Aktualizowanie zasad protokołu klienta i wywłasu</span><span class="sxs-lookup"><span data-stu-id="d5116-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="d5116-113">To polecenie aktualizuje zasady protokołu klienta i eksmisji bazy danych dla funkcji Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="d5116-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d5116-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5116-114">PARAMETERS</span></span>

### <span data-ttu-id="d5116-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d5116-115">-AsJob</span></span>
<span data-ttu-id="d5116-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d5116-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d5116-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d5116-117">-ClientProtocol</span></span>
<span data-ttu-id="d5116-118">Określa, czy klienci redis mogą łączyć się przy użyciu protokołów TLS-encrypted, czy zwykłego tekstu redis.</span><span class="sxs-lookup"><span data-stu-id="d5116-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="d5116-119">Wartością domyślną jest szyfrowanie TLS.</span><span class="sxs-lookup"><span data-stu-id="d5116-119">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5116-120">- ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="d5116-120">-ClusteringPolicy</span></span>
<span data-ttu-id="d5116-121">Zasady klastrowania — domyślne ustawienie to OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="d5116-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="d5116-122">Określony w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="d5116-122">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5116-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d5116-123">-ClusterName</span></span>
<span data-ttu-id="d5116-124">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d5116-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="d5116-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5116-125">-DefaultProfile</span></span>
<span data-ttu-id="d5116-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5116-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5116-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5116-127">-EvictionPolicy</span></span>
<span data-ttu-id="d5116-128">Zasady ponownego wywłasowania — wartość domyślna to NietrwałaLRU</span><span class="sxs-lookup"><span data-stu-id="d5116-128">Redis eviction policy - default is VolatileLRU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5116-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5116-129">-InputObject</span></span>
<span data-ttu-id="d5116-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d5116-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5116-131">— Moduł</span><span class="sxs-lookup"><span data-stu-id="d5116-131">-Module</span></span>
<span data-ttu-id="d5116-132">Opcjonalny zestaw modułów redis umożliwiających włączenie w tej bazie danych — moduły można dodawać tylko podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="d5116-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="d5116-133">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach modułu i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="d5116-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5116-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5116-134">-NoWait</span></span>
<span data-ttu-id="d5116-135">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d5116-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5116-136">— Port</span><span class="sxs-lookup"><span data-stu-id="d5116-136">-Port</span></span>
<span data-ttu-id="d5116-137">Port TCP punktu końcowego bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d5116-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="d5116-138">Określony w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="d5116-138">Specified at create time.</span></span>
<span data-ttu-id="d5116-139">Domyślnie jest to dostępny port.</span><span class="sxs-lookup"><span data-stu-id="d5116-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="d5116-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5116-140">-ResourceGroupName</span></span>
<span data-ttu-id="d5116-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5116-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5116-142">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5116-142">-SubscriptionId</span></span>
<span data-ttu-id="d5116-143">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5116-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5116-144">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d5116-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5116-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5116-145">-Confirm</span></span>
<span data-ttu-id="d5116-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5116-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5116-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5116-147">-WhatIf</span></span>
<span data-ttu-id="d5116-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5116-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5116-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5116-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5116-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5116-150">CommonParameters</span></span>
<span data-ttu-id="d5116-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5116-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5116-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5116-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5116-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5116-153">INPUTS</span></span>

### <span data-ttu-id="d5116-154">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="d5116-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="d5116-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5116-155">OUTPUTS</span></span>

### <span data-ttu-id="d5116-156">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="d5116-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="d5116-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5116-157">NOTES</span></span>

<span data-ttu-id="d5116-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d5116-158">ALIASES</span></span>

<span data-ttu-id="d5116-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5116-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5116-160">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d5116-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5116-161">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5116-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5116-162">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d5116-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5116-163">`[ClusterName <String>]`: nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d5116-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="d5116-164">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d5116-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d5116-165">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d5116-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5116-166">`[Location <String>]`: region, w który znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="d5116-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="d5116-167">`[OperationId <String>]`: czas trwania identyfikator unikatowy.</span><span class="sxs-lookup"><span data-stu-id="d5116-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="d5116-168">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d5116-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="d5116-169">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5116-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d5116-170">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5116-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d5116-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d5116-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d5116-172">MODULE <IModule[]>: Opcjonalny zestaw modułów redis umożliwiających włączenie w tej bazie danych — moduły można dodawać tylko podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="d5116-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="d5116-173">`Name <String>`: nazwa modułu, na przykład "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="d5116-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="d5116-174">`[Arg <String>]`: Opcje konfiguracji modułu, na przykład "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="d5116-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="d5116-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5116-175">RELATED LINKS</span></span>

