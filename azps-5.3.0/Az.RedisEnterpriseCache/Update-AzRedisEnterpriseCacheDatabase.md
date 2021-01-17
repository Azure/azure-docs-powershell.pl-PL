---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378156"
---
# <span data-ttu-id="8da3d-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="8da3d-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="8da3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8da3d-102">SYNOPSIS</span></span>
<span data-ttu-id="8da3d-103">Aktualizowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="8da3d-103">Updates a database</span></span>

## <span data-ttu-id="8da3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8da3d-104">SYNTAX</span></span>

### <span data-ttu-id="8da3d-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8da3d-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8da3d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8da3d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8da3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8da3d-107">DESCRIPTION</span></span>
<span data-ttu-id="8da3d-108">Aktualizowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="8da3d-108">Updates a database</span></span>

## <span data-ttu-id="8da3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8da3d-109">EXAMPLES</span></span>

### <span data-ttu-id="8da3d-110">Przykład 1: protokół Client Update</span><span class="sxs-lookup"><span data-stu-id="8da3d-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="8da3d-111">To polecenie aktualizuje protokół klienta bazy danych dla pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="8da3d-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="8da3d-112">Przykład 2: aktualizowanie protokołu klienta i zasad wykluczania</span><span class="sxs-lookup"><span data-stu-id="8da3d-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="8da3d-113">To polecenie aktualizuje zasady protokołu klienta i wykluczania bazy danych dla pamięci podręcznej Redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="8da3d-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="8da3d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da3d-114">PARAMETERS</span></span>

### <span data-ttu-id="8da3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da3d-115">-AsJob</span></span>
<span data-ttu-id="8da3d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8da3d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8da3d-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="8da3d-117">-ClientProtocol</span></span>
<span data-ttu-id="8da3d-118">Określa, czy klienci Redis mogą łączyć się przy użyciu protokołów szyfrowania TLS lub Redis.</span><span class="sxs-lookup"><span data-stu-id="8da3d-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="8da3d-119">Wartość domyślna to TLS-Encrypted.</span><span class="sxs-lookup"><span data-stu-id="8da3d-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="8da3d-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="8da3d-120">-ClusteringPolicy</span></span>
<span data-ttu-id="8da3d-121">Zasady klastrowania — domyślnie OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="8da3d-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="8da3d-122">Określone w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="8da3d-122">Specified at create time.</span></span>

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

### <span data-ttu-id="8da3d-123">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="8da3d-123">-ClusterName</span></span>
<span data-ttu-id="8da3d-124">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="8da3d-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="8da3d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da3d-125">-DefaultProfile</span></span>
<span data-ttu-id="8da3d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8da3d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da3d-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="8da3d-127">-EvictionPolicy</span></span>
<span data-ttu-id="8da3d-128">Zasady wykluczania Redis-domyślnie VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="8da3d-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="8da3d-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8da3d-129">-InputObject</span></span>
<span data-ttu-id="8da3d-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8da3d-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8da3d-131">-Module</span><span class="sxs-lookup"><span data-stu-id="8da3d-131">-Module</span></span>
<span data-ttu-id="8da3d-132">Opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="8da3d-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="8da3d-133">Aby skonstruować, zobacz sekcję notatki dla właściwości modułu i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8da3d-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="8da3d-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8da3d-134">-NoWait</span></span>
<span data-ttu-id="8da3d-135">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8da3d-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8da3d-136">-Port</span><span class="sxs-lookup"><span data-stu-id="8da3d-136">-Port</span></span>
<span data-ttu-id="8da3d-137">Port TCP punktu końcowego bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8da3d-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="8da3d-138">Określone w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="8da3d-138">Specified at create time.</span></span>
<span data-ttu-id="8da3d-139">Domyślnie jest to dostępny port.</span><span class="sxs-lookup"><span data-stu-id="8da3d-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="8da3d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da3d-140">-ResourceGroupName</span></span>
<span data-ttu-id="8da3d-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8da3d-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="8da3d-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8da3d-142">-SubscriptionId</span></span>
<span data-ttu-id="8da3d-143">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8da3d-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8da3d-144">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8da3d-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8da3d-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8da3d-145">-Confirm</span></span>
<span data-ttu-id="8da3d-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da3d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da3d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da3d-147">-WhatIf</span></span>
<span data-ttu-id="8da3d-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da3d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da3d-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8da3d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da3d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da3d-150">CommonParameters</span></span>
<span data-ttu-id="8da3d-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da3d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da3d-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da3d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da3d-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8da3d-153">INPUTS</span></span>

### <span data-ttu-id="8da3d-154">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="8da3d-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="8da3d-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8da3d-155">OUTPUTS</span></span>

### <span data-ttu-id="8da3d-156">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="8da3d-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="8da3d-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8da3d-157">NOTES</span></span>

<span data-ttu-id="8da3d-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8da3d-158">ALIASES</span></span>

<span data-ttu-id="8da3d-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da3d-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8da3d-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8da3d-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8da3d-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8da3d-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8da3d-162">INPUTobject <IRedisEnterpriseCacheIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8da3d-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8da3d-163">`[ClusterName <String>]`: Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="8da3d-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="8da3d-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8da3d-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8da3d-165">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8da3d-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8da3d-166">`[Location <String>]`: Region, w którym znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="8da3d-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="8da3d-167">`[OperationId <String>]`: Unikatowy identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="8da3d-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="8da3d-168">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8da3d-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="8da3d-169">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8da3d-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8da3d-170">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8da3d-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8da3d-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8da3d-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="8da3d-172">Moduł <IModule [] >: opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="8da3d-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="8da3d-173">`Name <String>`: Nazwa modułu, na przykład "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="8da3d-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="8da3d-174">`[Arg <String>]`: Opcje konfiguracji modułu, na przykład "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="8da3d-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="8da3d-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8da3d-175">RELATED LINKS</span></span>

