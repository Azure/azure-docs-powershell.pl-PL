---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490701"
---
# <span data-ttu-id="319d3-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="319d3-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="319d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="319d3-102">SYNOPSIS</span></span>
<span data-ttu-id="319d3-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="319d3-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="319d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="319d3-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="319d3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="319d3-105">DESCRIPTION</span></span>
<span data-ttu-id="319d3-106">Polecenie cmdlet **Set-AzRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="319d3-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="319d3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="319d3-107">EXAMPLES</span></span>

### <span data-ttu-id="319d3-108">Przykład 1: modyfikowanie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="319d3-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="319d3-109">To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="319d3-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="319d3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="319d3-110">PARAMETERS</span></span>

### <span data-ttu-id="319d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319d3-111">-DefaultProfile</span></span>
<span data-ttu-id="319d3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="319d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="319d3-113">-EnableNonSslPort</span></span>
<span data-ttu-id="319d3-114">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="319d3-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="319d3-115">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="319d3-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="319d3-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="319d3-117">Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="319d3-117">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="319d3-118">-Name</span></span>
<span data-ttu-id="319d3-119">Określa nazwę pamięci podręcznej Redis do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="319d3-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="319d3-120">-RedisConfiguration</span></span>
<span data-ttu-id="319d3-121">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="319d3-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="319d3-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="319d3-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="319d3-123">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="319d3-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="319d3-124">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="319d3-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="319d3-125">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-125">Premium tier only.</span></span>
- <span data-ttu-id="319d3-126">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="319d3-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="319d3-127">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="319d3-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="319d3-128">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-128">Premium tier only.</span></span>
- <span data-ttu-id="319d3-129">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="319d3-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="319d3-130">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="319d3-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="319d3-131">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-131">Premium tier only.</span></span> 
- <span data-ttu-id="319d3-132">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="319d3-132">maxmemory-reserved.</span></span>
<span data-ttu-id="319d3-133">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="319d3-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="319d3-134">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-135">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="319d3-135">maxmemory-policy.</span></span>
<span data-ttu-id="319d3-136">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="319d3-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="319d3-137">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="319d3-137">All pricing tiers.</span></span> 
- <span data-ttu-id="319d3-138">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="319d3-138">notify-keyspace-events.</span></span>
<span data-ttu-id="319d3-139">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="319d3-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="319d3-140">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="319d3-141">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="319d3-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="319d3-142">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="319d3-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="319d3-143">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-144">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="319d3-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="319d3-145">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="319d3-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="319d3-146">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-147">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="319d3-147">set-max-intset-entries.</span></span>
<span data-ttu-id="319d3-148">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="319d3-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="319d3-149">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-150">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="319d3-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="319d3-151">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="319d3-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="319d3-152">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-153">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="319d3-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="319d3-154">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="319d3-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="319d3-155">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="319d3-156">baz danych.</span><span class="sxs-lookup"><span data-stu-id="319d3-156">databases.</span></span>
<span data-ttu-id="319d3-157">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="319d3-157">Configures the number of databases.</span></span>
<span data-ttu-id="319d3-158">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="319d3-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="319d3-159">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="319d3-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="319d3-160">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="319d3-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319d3-161">-ResourceGroupName</span></span>
<span data-ttu-id="319d3-162">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="319d3-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="319d3-163">-ShardCount</span></span>
<span data-ttu-id="319d3-164">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="319d3-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-165">-Size</span><span class="sxs-lookup"><span data-stu-id="319d3-165">-Size</span></span>
<span data-ttu-id="319d3-166">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="319d3-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="319d3-167">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="319d3-167">Valid values are:</span></span> 
- <span data-ttu-id="319d3-168">Punkt</span><span class="sxs-lookup"><span data-stu-id="319d3-168">P1</span></span>
- <span data-ttu-id="319d3-169">Punktu</span><span class="sxs-lookup"><span data-stu-id="319d3-169">P2</span></span>
- <span data-ttu-id="319d3-170">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="319d3-170">P3</span></span>
- <span data-ttu-id="319d3-171">P4</span><span class="sxs-lookup"><span data-stu-id="319d3-171">P4</span></span>
- <span data-ttu-id="319d3-172">P5</span><span class="sxs-lookup"><span data-stu-id="319d3-172">P5</span></span>
- <span data-ttu-id="319d3-173">C0</span><span class="sxs-lookup"><span data-stu-id="319d3-173">C0</span></span>
- <span data-ttu-id="319d3-174">C1</span><span class="sxs-lookup"><span data-stu-id="319d3-174">C1</span></span>
- <span data-ttu-id="319d3-175">C2</span><span class="sxs-lookup"><span data-stu-id="319d3-175">C2</span></span>
- <span data-ttu-id="319d3-176">C3</span><span class="sxs-lookup"><span data-stu-id="319d3-176">C3</span></span>
- <span data-ttu-id="319d3-177">C4</span><span class="sxs-lookup"><span data-stu-id="319d3-177">C4</span></span>
- <span data-ttu-id="319d3-178">C5</span><span class="sxs-lookup"><span data-stu-id="319d3-178">C5</span></span>
- <span data-ttu-id="319d3-179">C6</span><span class="sxs-lookup"><span data-stu-id="319d3-179">C6</span></span>
- <span data-ttu-id="319d3-180">250MB</span><span class="sxs-lookup"><span data-stu-id="319d3-180">250MB</span></span>
- <span data-ttu-id="319d3-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="319d3-181">1GB</span></span>
- <span data-ttu-id="319d3-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="319d3-182">2.5GB</span></span>
- <span data-ttu-id="319d3-183">6GB</span><span class="sxs-lookup"><span data-stu-id="319d3-183">6GB</span></span>
- <span data-ttu-id="319d3-184">13GB</span><span class="sxs-lookup"><span data-stu-id="319d3-184">13GB</span></span>
- <span data-ttu-id="319d3-185">26GB</span><span class="sxs-lookup"><span data-stu-id="319d3-185">26GB</span></span>
- <span data-ttu-id="319d3-186">53GB</span><span class="sxs-lookup"><span data-stu-id="319d3-186">53GB</span></span>
- <span data-ttu-id="319d3-187">120 GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="319d3-187">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="319d3-188">-Sku</span></span>
<span data-ttu-id="319d3-189">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="319d3-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="319d3-190">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="319d3-190">Valid values are:</span></span> 
- <span data-ttu-id="319d3-191">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="319d3-191">Basic</span></span>
- <span data-ttu-id="319d3-192">Standard</span><span class="sxs-lookup"><span data-stu-id="319d3-192">Standard</span></span>
- <span data-ttu-id="319d3-193">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="319d3-193">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="319d3-194">-Tag</span></span>
<span data-ttu-id="319d3-195">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="319d3-195">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="319d3-196">-TenantSettings</span></span>
<span data-ttu-id="319d3-197">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="319d3-197">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319d3-198">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="319d3-198">-Confirm</span></span>
<span data-ttu-id="319d3-199">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="319d3-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319d3-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319d3-200">-WhatIf</span></span>
<span data-ttu-id="319d3-201">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="319d3-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="319d3-202">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="319d3-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319d3-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319d3-203">CommonParameters</span></span>
<span data-ttu-id="319d3-204">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319d3-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319d3-205">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="319d3-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319d3-206">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="319d3-206">INPUTS</span></span>

### <span data-ttu-id="319d3-207">System. String</span><span class="sxs-lookup"><span data-stu-id="319d3-207">System.String</span></span>

### <span data-ttu-id="319d3-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="319d3-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="319d3-209">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="319d3-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="319d3-210">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="319d3-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="319d3-211">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="319d3-211">OUTPUTS</span></span>

### <span data-ttu-id="319d3-212">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="319d3-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="319d3-213">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="319d3-213">NOTES</span></span>

## <span data-ttu-id="319d3-214">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="319d3-214">RELATED LINKS</span></span>

[<span data-ttu-id="319d3-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="319d3-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="319d3-216">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="319d3-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="319d3-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="319d3-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


