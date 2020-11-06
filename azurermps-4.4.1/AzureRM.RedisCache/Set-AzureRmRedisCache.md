---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543040"
---
# <span data-ttu-id="26049-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="26049-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="26049-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26049-102">SYNOPSIS</span></span>
<span data-ttu-id="26049-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="26049-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26049-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26049-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26049-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26049-105">DESCRIPTION</span></span>
<span data-ttu-id="26049-106">Polecenie cmdlet **Set-AzureRmRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="26049-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="26049-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26049-107">EXAMPLES</span></span>

### <span data-ttu-id="26049-108">Przykład 1: modyfikowanie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="26049-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
```

<span data-ttu-id="26049-109">To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="26049-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="26049-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26049-110">PARAMETERS</span></span>

### <span data-ttu-id="26049-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="26049-111">-EnableNonSslPort</span></span>
<span data-ttu-id="26049-112">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="26049-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="26049-113">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="26049-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="26049-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="26049-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="26049-115">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="26049-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="26049-116">Użyj parametru *RedisConfiguration* , aby ustawić maxmemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="26049-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="26049-117">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="26049-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="26049-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26049-118">-Name</span></span>
<span data-ttu-id="26049-119">Określa nazwę pamięci podręcznej Redis do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="26049-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="26049-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="26049-120">-RedisConfiguration</span></span>
<span data-ttu-id="26049-121">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="26049-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="26049-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26049-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26049-123">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="26049-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="26049-124">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="26049-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="26049-125">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-125">Premium tier only.</span></span>
- <span data-ttu-id="26049-126">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="26049-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="26049-127">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="26049-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="26049-128">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-128">Premium tier only.</span></span>
- <span data-ttu-id="26049-129">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="26049-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="26049-130">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="26049-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="26049-131">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-131">Premium tier only.</span></span> 
- <span data-ttu-id="26049-132">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="26049-132">maxmemory-reserved.</span></span>
<span data-ttu-id="26049-133">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="26049-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="26049-134">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-135">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="26049-135">maxmemory-policy.</span></span>
<span data-ttu-id="26049-136">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="26049-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="26049-137">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="26049-137">All pricing tiers.</span></span> 
- <span data-ttu-id="26049-138">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="26049-138">notify-keyspace-events.</span></span>
<span data-ttu-id="26049-139">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="26049-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="26049-140">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="26049-141">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="26049-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="26049-142">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="26049-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26049-143">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-144">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="26049-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="26049-145">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="26049-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26049-146">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-147">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="26049-147">set-max-intset-entries.</span></span>
<span data-ttu-id="26049-148">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="26049-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26049-149">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-150">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="26049-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="26049-151">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="26049-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26049-152">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-153">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="26049-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="26049-154">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="26049-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26049-155">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26049-156">baz danych.</span><span class="sxs-lookup"><span data-stu-id="26049-156">databases.</span></span>
<span data-ttu-id="26049-157">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="26049-157">Configures the number of databases.</span></span>
<span data-ttu-id="26049-158">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="26049-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="26049-159">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="26049-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="26049-160">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="26049-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="26049-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26049-161">-ResourceGroupName</span></span>
<span data-ttu-id="26049-162">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="26049-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="26049-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="26049-163">-ShardCount</span></span>
<span data-ttu-id="26049-164">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="26049-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="26049-165">-Size</span><span class="sxs-lookup"><span data-stu-id="26049-165">-Size</span></span>
<span data-ttu-id="26049-166">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="26049-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="26049-167">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="26049-167">Valid values are:</span></span> 

- <span data-ttu-id="26049-168">Punkt</span><span class="sxs-lookup"><span data-stu-id="26049-168">P1</span></span>
- <span data-ttu-id="26049-169">Punktu</span><span class="sxs-lookup"><span data-stu-id="26049-169">P2</span></span>
- <span data-ttu-id="26049-170">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="26049-170">P3</span></span>
- <span data-ttu-id="26049-171">P4</span><span class="sxs-lookup"><span data-stu-id="26049-171">P4</span></span>
- <span data-ttu-id="26049-172">C0</span><span class="sxs-lookup"><span data-stu-id="26049-172">C0</span></span>
- <span data-ttu-id="26049-173">C1</span><span class="sxs-lookup"><span data-stu-id="26049-173">C1</span></span>
- <span data-ttu-id="26049-174">C2</span><span class="sxs-lookup"><span data-stu-id="26049-174">C2</span></span>
- <span data-ttu-id="26049-175">C3</span><span class="sxs-lookup"><span data-stu-id="26049-175">C3</span></span>
- <span data-ttu-id="26049-176">C4</span><span class="sxs-lookup"><span data-stu-id="26049-176">C4</span></span>
- <span data-ttu-id="26049-177">C5</span><span class="sxs-lookup"><span data-stu-id="26049-177">C5</span></span>
- <span data-ttu-id="26049-178">C6</span><span class="sxs-lookup"><span data-stu-id="26049-178">C6</span></span>
- <span data-ttu-id="26049-179">250MB</span><span class="sxs-lookup"><span data-stu-id="26049-179">250MB</span></span>
- <span data-ttu-id="26049-180">1 GB</span><span class="sxs-lookup"><span data-stu-id="26049-180">1GB</span></span>
- <span data-ttu-id="26049-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="26049-181">2.5GB</span></span>
- <span data-ttu-id="26049-182">6GB</span><span class="sxs-lookup"><span data-stu-id="26049-182">6GB</span></span>
- <span data-ttu-id="26049-183">13GB</span><span class="sxs-lookup"><span data-stu-id="26049-183">13GB</span></span>
- <span data-ttu-id="26049-184">26GB</span><span class="sxs-lookup"><span data-stu-id="26049-184">26GB</span></span>
- <span data-ttu-id="26049-185">53GB</span><span class="sxs-lookup"><span data-stu-id="26049-185">53GB</span></span>

<span data-ttu-id="26049-186">Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="26049-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26049-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="26049-187">-Sku</span></span>
<span data-ttu-id="26049-188">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="26049-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="26049-189">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="26049-189">Valid values are:</span></span> 

- <span data-ttu-id="26049-190">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="26049-190">Basic</span></span>
- <span data-ttu-id="26049-191">Standard</span><span class="sxs-lookup"><span data-stu-id="26049-191">Standard</span></span>
- <span data-ttu-id="26049-192">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="26049-192">Premium</span></span>

<span data-ttu-id="26049-193">Wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="26049-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="26049-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="26049-194">-TenantSettings</span></span>
<span data-ttu-id="26049-195">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="26049-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="26049-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26049-196">-DefaultProfile</span></span>
<span data-ttu-id="26049-197">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26049-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26049-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26049-198">CommonParameters</span></span>
<span data-ttu-id="26049-199">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26049-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26049-200">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26049-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26049-201">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26049-201">INPUTS</span></span>

### <span data-ttu-id="26049-202">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26049-202">None</span></span>
<span data-ttu-id="26049-203">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="26049-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="26049-204">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26049-204">OUTPUTS</span></span>

### <span data-ttu-id="26049-205">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="26049-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="26049-206">Zwraca wszystkie atrybuty pamięci podręcznej Redis, w tym klucze podstawowych i pomocniczych dostępu.</span><span class="sxs-lookup"><span data-stu-id="26049-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="26049-207">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26049-207">NOTES</span></span>

## <span data-ttu-id="26049-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26049-208">RELATED LINKS</span></span>

[<span data-ttu-id="26049-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="26049-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="26049-210">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="26049-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="26049-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="26049-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


