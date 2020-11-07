---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871963"
---
# <span data-ttu-id="b6889-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6889-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="b6889-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6889-102">SYNOPSIS</span></span>
<span data-ttu-id="b6889-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="b6889-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="b6889-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6889-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6889-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6889-105">DESCRIPTION</span></span>
<span data-ttu-id="b6889-106">Polecenie cmdlet **Set-AzRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b6889-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="b6889-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6889-107">EXAMPLES</span></span>

### <span data-ttu-id="b6889-108">Przykład 1: modyfikowanie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="b6889-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="b6889-109">To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="b6889-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="b6889-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6889-110">PARAMETERS</span></span>

### <span data-ttu-id="b6889-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6889-111">-DefaultProfile</span></span>
<span data-ttu-id="b6889-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6889-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6889-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b6889-113">-EnableNonSslPort</span></span>
<span data-ttu-id="b6889-114">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="b6889-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b6889-115">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="b6889-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="b6889-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6889-116">-Name</span></span>
<span data-ttu-id="b6889-117">Określa nazwę pamięci podręcznej Redis do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b6889-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="b6889-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6889-118">-RedisConfiguration</span></span>
<span data-ttu-id="b6889-119">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="b6889-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b6889-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6889-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6889-121">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b6889-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="b6889-122">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b6889-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b6889-123">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-123">Premium tier only.</span></span>
- <span data-ttu-id="b6889-124">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="b6889-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b6889-125">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="b6889-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b6889-126">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-126">Premium tier only.</span></span>
- <span data-ttu-id="b6889-127">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b6889-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="b6889-128">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="b6889-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b6889-129">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-129">Premium tier only.</span></span> 
- <span data-ttu-id="b6889-130">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="b6889-130">maxmemory-reserved.</span></span>
<span data-ttu-id="b6889-131">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b6889-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b6889-132">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-133">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="b6889-133">maxmemory-policy.</span></span>
<span data-ttu-id="b6889-134">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b6889-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b6889-135">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="b6889-135">All pricing tiers.</span></span> 
- <span data-ttu-id="b6889-136">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="b6889-136">notify-keyspace-events.</span></span>
<span data-ttu-id="b6889-137">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="b6889-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="b6889-138">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b6889-139">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="b6889-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b6889-140">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="b6889-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6889-141">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-142">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="b6889-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b6889-143">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="b6889-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6889-144">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-145">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="b6889-145">set-max-intset-entries.</span></span>
<span data-ttu-id="b6889-146">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="b6889-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6889-147">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-148">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="b6889-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b6889-149">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="b6889-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6889-150">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-151">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="b6889-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b6889-152">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="b6889-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6889-153">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6889-154">baz danych.</span><span class="sxs-lookup"><span data-stu-id="b6889-154">databases.</span></span>
<span data-ttu-id="b6889-155">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="b6889-155">Configures the number of databases.</span></span>
<span data-ttu-id="b6889-156">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b6889-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b6889-157">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="b6889-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="b6889-158">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b6889-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="b6889-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6889-159">-ResourceGroupName</span></span>
<span data-ttu-id="b6889-160">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="b6889-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="b6889-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b6889-161">-ShardCount</span></span>
<span data-ttu-id="b6889-162">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="b6889-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="b6889-163">-Size</span><span class="sxs-lookup"><span data-stu-id="b6889-163">-Size</span></span>
<span data-ttu-id="b6889-164">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="b6889-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b6889-165">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b6889-165">Valid values are:</span></span> 
- <span data-ttu-id="b6889-166">Punkt</span><span class="sxs-lookup"><span data-stu-id="b6889-166">P1</span></span>
- <span data-ttu-id="b6889-167">Punktu</span><span class="sxs-lookup"><span data-stu-id="b6889-167">P2</span></span>
- <span data-ttu-id="b6889-168">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="b6889-168">P3</span></span>
- <span data-ttu-id="b6889-169">P4</span><span class="sxs-lookup"><span data-stu-id="b6889-169">P4</span></span>
- <span data-ttu-id="b6889-170">P5</span><span class="sxs-lookup"><span data-stu-id="b6889-170">P5</span></span>
- <span data-ttu-id="b6889-171">C0</span><span class="sxs-lookup"><span data-stu-id="b6889-171">C0</span></span>
- <span data-ttu-id="b6889-172">C1</span><span class="sxs-lookup"><span data-stu-id="b6889-172">C1</span></span>
- <span data-ttu-id="b6889-173">C2</span><span class="sxs-lookup"><span data-stu-id="b6889-173">C2</span></span>
- <span data-ttu-id="b6889-174">C3</span><span class="sxs-lookup"><span data-stu-id="b6889-174">C3</span></span>
- <span data-ttu-id="b6889-175">C4</span><span class="sxs-lookup"><span data-stu-id="b6889-175">C4</span></span>
- <span data-ttu-id="b6889-176">C5</span><span class="sxs-lookup"><span data-stu-id="b6889-176">C5</span></span>
- <span data-ttu-id="b6889-177">C6</span><span class="sxs-lookup"><span data-stu-id="b6889-177">C6</span></span>
- <span data-ttu-id="b6889-178">250MB</span><span class="sxs-lookup"><span data-stu-id="b6889-178">250MB</span></span>
- <span data-ttu-id="b6889-179">1 GB</span><span class="sxs-lookup"><span data-stu-id="b6889-179">1GB</span></span>
- <span data-ttu-id="b6889-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="b6889-180">2.5GB</span></span>
- <span data-ttu-id="b6889-181">6GB</span><span class="sxs-lookup"><span data-stu-id="b6889-181">6GB</span></span>
- <span data-ttu-id="b6889-182">13GB</span><span class="sxs-lookup"><span data-stu-id="b6889-182">13GB</span></span>
- <span data-ttu-id="b6889-183">26GB</span><span class="sxs-lookup"><span data-stu-id="b6889-183">26GB</span></span>
- <span data-ttu-id="b6889-184">53GB</span><span class="sxs-lookup"><span data-stu-id="b6889-184">53GB</span></span>
- <span data-ttu-id="b6889-185">120 GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="b6889-185">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="b6889-186">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6889-186">-Sku</span></span>
<span data-ttu-id="b6889-187">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b6889-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b6889-188">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b6889-188">Valid values are:</span></span> 
- <span data-ttu-id="b6889-189">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="b6889-189">Basic</span></span>
- <span data-ttu-id="b6889-190">Standard</span><span class="sxs-lookup"><span data-stu-id="b6889-190">Standard</span></span>
- <span data-ttu-id="b6889-191">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="b6889-191">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="b6889-192">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6889-192">-Tag</span></span>
<span data-ttu-id="b6889-193">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="b6889-193">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="b6889-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b6889-194">-TenantSettings</span></span>
<span data-ttu-id="b6889-195">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="b6889-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="b6889-196">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6889-196">-Confirm</span></span>
<span data-ttu-id="b6889-197">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6889-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6889-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6889-198">-WhatIf</span></span>
<span data-ttu-id="b6889-199">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6889-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6889-200">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6889-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6889-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6889-201">CommonParameters</span></span>
<span data-ttu-id="b6889-202">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6889-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6889-203">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6889-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6889-204">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6889-204">INPUTS</span></span>

### <span data-ttu-id="b6889-205">System. String</span><span class="sxs-lookup"><span data-stu-id="b6889-205">System.String</span></span>

### <span data-ttu-id="b6889-206">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6889-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b6889-207">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6889-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6889-208">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6889-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b6889-209">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6889-209">OUTPUTS</span></span>

### <span data-ttu-id="b6889-210">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b6889-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="b6889-211">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6889-211">NOTES</span></span>

## <span data-ttu-id="b6889-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6889-212">RELATED LINKS</span></span>

[<span data-ttu-id="b6889-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6889-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="b6889-214">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6889-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b6889-215">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6889-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


