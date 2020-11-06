---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544164"
---
# <span data-ttu-id="4e68a-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e68a-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="4e68a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e68a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e68a-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="4e68a-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e68a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e68a-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e68a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e68a-105">DESCRIPTION</span></span>
<span data-ttu-id="4e68a-106">Polecenie cmdlet **Set-AzureRmRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="4e68a-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="4e68a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e68a-107">EXAMPLES</span></span>

### <span data-ttu-id="4e68a-108">Przykład 1: modyfikowanie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="4e68a-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="4e68a-109">To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="4e68a-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="4e68a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e68a-110">PARAMETERS</span></span>

### <span data-ttu-id="4e68a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e68a-111">-DefaultProfile</span></span>
<span data-ttu-id="4e68a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e68a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="4e68a-113">-EnableNonSslPort</span></span>
<span data-ttu-id="4e68a-114">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="4e68a-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="4e68a-115">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="4e68a-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="4e68a-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="4e68a-117">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="4e68a-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="4e68a-118">Użyj parametru *RedisConfiguration* , aby ustawić maxmemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="4e68a-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="4e68a-119">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4e68a-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e68a-120">-Name</span></span>
<span data-ttu-id="4e68a-121">Określa nazwę pamięci podręcznej Redis do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4e68a-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e68a-122">-RedisConfiguration</span></span>
<span data-ttu-id="4e68a-123">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="4e68a-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="4e68a-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e68a-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e68a-125">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4e68a-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="4e68a-126">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="4e68a-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="4e68a-127">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-127">Premium tier only.</span></span>
- <span data-ttu-id="4e68a-128">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="4e68a-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="4e68a-129">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="4e68a-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="4e68a-130">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-130">Premium tier only.</span></span>
- <span data-ttu-id="4e68a-131">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="4e68a-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="4e68a-132">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="4e68a-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="4e68a-133">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-133">Premium tier only.</span></span> 
- <span data-ttu-id="4e68a-134">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="4e68a-134">maxmemory-reserved.</span></span>
<span data-ttu-id="4e68a-135">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4e68a-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="4e68a-136">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-137">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="4e68a-137">maxmemory-policy.</span></span>
<span data-ttu-id="4e68a-138">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4e68a-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="4e68a-139">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="4e68a-139">All pricing tiers.</span></span> 
- <span data-ttu-id="4e68a-140">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="4e68a-140">notify-keyspace-events.</span></span>
<span data-ttu-id="4e68a-141">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="4e68a-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="4e68a-142">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="4e68a-143">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4e68a-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="4e68a-144">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4e68a-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4e68a-145">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-146">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="4e68a-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="4e68a-147">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4e68a-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4e68a-148">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-149">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4e68a-149">set-max-intset-entries.</span></span>
<span data-ttu-id="4e68a-150">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4e68a-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4e68a-151">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-152">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4e68a-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="4e68a-153">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4e68a-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4e68a-154">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-155">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="4e68a-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="4e68a-156">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4e68a-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4e68a-157">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4e68a-158">baz danych.</span><span class="sxs-lookup"><span data-stu-id="4e68a-158">databases.</span></span>
<span data-ttu-id="4e68a-159">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="4e68a-159">Configures the number of databases.</span></span>
<span data-ttu-id="4e68a-160">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4e68a-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="4e68a-161">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4e68a-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="4e68a-162">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="4e68a-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e68a-163">-ResourceGroupName</span></span>
<span data-ttu-id="4e68a-164">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="4e68a-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="4e68a-165">-ShardCount</span></span>
<span data-ttu-id="4e68a-166">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="4e68a-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-167">-Size</span><span class="sxs-lookup"><span data-stu-id="4e68a-167">-Size</span></span>
<span data-ttu-id="4e68a-168">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="4e68a-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="4e68a-169">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4e68a-169">Valid values are:</span></span> 

- <span data-ttu-id="4e68a-170">Punkt</span><span class="sxs-lookup"><span data-stu-id="4e68a-170">P1</span></span>
- <span data-ttu-id="4e68a-171">Punktu</span><span class="sxs-lookup"><span data-stu-id="4e68a-171">P2</span></span>
- <span data-ttu-id="4e68a-172">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="4e68a-172">P3</span></span>
- <span data-ttu-id="4e68a-173">P4</span><span class="sxs-lookup"><span data-stu-id="4e68a-173">P4</span></span>
- <span data-ttu-id="4e68a-174">C0</span><span class="sxs-lookup"><span data-stu-id="4e68a-174">C0</span></span>
- <span data-ttu-id="4e68a-175">C1</span><span class="sxs-lookup"><span data-stu-id="4e68a-175">C1</span></span>
- <span data-ttu-id="4e68a-176">C2</span><span class="sxs-lookup"><span data-stu-id="4e68a-176">C2</span></span>
- <span data-ttu-id="4e68a-177">C3</span><span class="sxs-lookup"><span data-stu-id="4e68a-177">C3</span></span>
- <span data-ttu-id="4e68a-178">C4</span><span class="sxs-lookup"><span data-stu-id="4e68a-178">C4</span></span>
- <span data-ttu-id="4e68a-179">C5</span><span class="sxs-lookup"><span data-stu-id="4e68a-179">C5</span></span>
- <span data-ttu-id="4e68a-180">C6</span><span class="sxs-lookup"><span data-stu-id="4e68a-180">C6</span></span>
- <span data-ttu-id="4e68a-181">250MB</span><span class="sxs-lookup"><span data-stu-id="4e68a-181">250MB</span></span>
- <span data-ttu-id="4e68a-182">1 GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-182">1GB</span></span>
- <span data-ttu-id="4e68a-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-183">2.5GB</span></span>
- <span data-ttu-id="4e68a-184">6GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-184">6GB</span></span>
- <span data-ttu-id="4e68a-185">13GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-185">13GB</span></span>
- <span data-ttu-id="4e68a-186">26GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-186">26GB</span></span>
- <span data-ttu-id="4e68a-187">53GB</span><span class="sxs-lookup"><span data-stu-id="4e68a-187">53GB</span></span>

<span data-ttu-id="4e68a-188">Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="4e68a-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="4e68a-189">-Sku</span></span>
<span data-ttu-id="4e68a-190">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4e68a-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="4e68a-191">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4e68a-191">Valid values are:</span></span> 

- <span data-ttu-id="4e68a-192">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="4e68a-192">Basic</span></span>
- <span data-ttu-id="4e68a-193">Standard</span><span class="sxs-lookup"><span data-stu-id="4e68a-193">Standard</span></span>
- <span data-ttu-id="4e68a-194">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="4e68a-194">Premium</span></span>

<span data-ttu-id="4e68a-195">Wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="4e68a-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-196">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e68a-196">-Tag</span></span>
<span data-ttu-id="4e68a-197">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="4e68a-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="4e68a-198">-TenantSettings</span></span>
<span data-ttu-id="4e68a-199">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="4e68a-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-200">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e68a-200">-Confirm</span></span>
<span data-ttu-id="4e68a-201">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e68a-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e68a-202">-WhatIf</span></span>
<span data-ttu-id="4e68a-203">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e68a-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e68a-204">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e68a-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68a-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e68a-205">CommonParameters</span></span>
<span data-ttu-id="4e68a-206">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e68a-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e68a-207">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e68a-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e68a-208">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e68a-208">INPUTS</span></span>

### <span data-ttu-id="4e68a-209">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4e68a-209">None</span></span>
<span data-ttu-id="4e68a-210">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="4e68a-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4e68a-211">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e68a-211">OUTPUTS</span></span>

### <span data-ttu-id="4e68a-212">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4e68a-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="4e68a-213">Zwraca wszystkie atrybuty pamięci podręcznej Redis, w tym klucze podstawowych i pomocniczych dostępu.</span><span class="sxs-lookup"><span data-stu-id="4e68a-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="4e68a-214">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e68a-214">NOTES</span></span>

## <span data-ttu-id="4e68a-215">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e68a-215">RELATED LINKS</span></span>

[<span data-ttu-id="4e68a-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e68a-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4e68a-217">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e68a-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4e68a-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e68a-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


