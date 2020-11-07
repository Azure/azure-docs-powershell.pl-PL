---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716890"
---
# <span data-ttu-id="3ee6d-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3ee6d-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="3ee6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ee6d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee6d-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ee6d-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ee6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ee6d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee6d-106">Polecenie cmdlet **New-AzureRmRedisCache** tworzy pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="3ee6d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ee6d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee6d-108">Przykład 1. tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="3ee6d-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="3ee6d-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="3ee6d-110">Przykład 2: Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="3ee6d-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="3ee6d-111">To polecenie tworzy pamięć podręczną Redis lub aktualizuje pamięć podręczną Redis, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="3ee6d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ee6d-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee6d-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="3ee6d-113">-EnableNonSslPort</span></span>
<span data-ttu-id="3ee6d-114">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="3ee6d-115">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="3ee6d-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="3ee6d-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3ee6d-116">-Location</span></span>
<span data-ttu-id="3ee6d-117">Określa lokalizację, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="3ee6d-118">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-118">Valid values are:</span></span> 

- <span data-ttu-id="3ee6d-119">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="3ee6d-119">North Central US</span></span>
- <span data-ttu-id="3ee6d-120">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="3ee6d-120">South Central US</span></span>
- <span data-ttu-id="3ee6d-121">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="3ee6d-121">Central US</span></span>
- <span data-ttu-id="3ee6d-122">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="3ee6d-122">West Europe</span></span>
- <span data-ttu-id="3ee6d-123">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="3ee6d-123">North Europe</span></span>
- <span data-ttu-id="3ee6d-124">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="3ee6d-124">West US</span></span>
- <span data-ttu-id="3ee6d-125">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="3ee6d-125">East US</span></span>
- <span data-ttu-id="3ee6d-126">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="3ee6d-126">East US 2</span></span>
- <span data-ttu-id="3ee6d-127">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="3ee6d-127">Japan East</span></span>
- <span data-ttu-id="3ee6d-128">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="3ee6d-128">Japan West</span></span>
- <span data-ttu-id="3ee6d-129">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="3ee6d-129">Brazil South</span></span>
- <span data-ttu-id="3ee6d-130">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3ee6d-130">Southeast Asia</span></span>
- <span data-ttu-id="3ee6d-131">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3ee6d-131">East Asia</span></span>
- <span data-ttu-id="3ee6d-132">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3ee6d-132">Australia East</span></span>
- <span data-ttu-id="3ee6d-133">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="3ee6d-133">Australia Southeast</span></span>

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

### <span data-ttu-id="3ee6d-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="3ee6d-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="3ee6d-135">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="3ee6d-136">Użyj parametru *RedisConfiguration* , aby ustawić maxmemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="3ee6d-137">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-137">For example:</span></span> 

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

### <span data-ttu-id="3ee6d-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ee6d-138">-Name</span></span>
<span data-ttu-id="3ee6d-139">Określa nazwę pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="3ee6d-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ee6d-140">-RedisConfiguration</span></span>
<span data-ttu-id="3ee6d-141">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="3ee6d-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ee6d-143">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="3ee6d-144">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="3ee6d-145">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-145">Premium tier only.</span></span>
- <span data-ttu-id="3ee6d-146">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="3ee6d-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="3ee6d-147">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="3ee6d-148">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-148">Premium tier only.</span></span>
- <span data-ttu-id="3ee6d-149">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="3ee6d-150">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="3ee6d-151">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-151">Premium tier only.</span></span> 
- <span data-ttu-id="3ee6d-152">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-152">maxmemory-reserved.</span></span>
<span data-ttu-id="3ee6d-153">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="3ee6d-154">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-155">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-155">maxmemory-policy.</span></span>
<span data-ttu-id="3ee6d-156">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="3ee6d-157">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-157">All pricing tiers.</span></span> 
- <span data-ttu-id="3ee6d-158">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-158">notify-keyspace-events.</span></span>
<span data-ttu-id="3ee6d-159">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="3ee6d-160">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-161">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="3ee6d-162">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3ee6d-163">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-164">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="3ee6d-165">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3ee6d-166">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-167">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-167">set-max-intset-entries.</span></span>
<span data-ttu-id="3ee6d-168">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3ee6d-169">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-170">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="3ee6d-171">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3ee6d-172">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-173">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="3ee6d-174">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3ee6d-175">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3ee6d-176">baz danych.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-176">databases.</span></span>
<span data-ttu-id="3ee6d-177">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-177">Configures the number of databases.</span></span>
<span data-ttu-id="3ee6d-178">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="3ee6d-179">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="3ee6d-180">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="3ee6d-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="3ee6d-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="3ee6d-181">-RedisVersion</span></span>
<span data-ttu-id="3ee6d-182">Ten parametr jest przestarzały i zostanie usunięty z przyszłych wersji.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="3ee6d-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee6d-183">-ResourceGroupName</span></span>
<span data-ttu-id="3ee6d-184">Określa nazwę grupy zasobów, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="3ee6d-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="3ee6d-185">-ShardCount</span></span>
<span data-ttu-id="3ee6d-186">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="3ee6d-187">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ee6d-188">jedno</span><span class="sxs-lookup"><span data-stu-id="3ee6d-188">1</span></span>
- <span data-ttu-id="3ee6d-189">2,6</span><span class="sxs-lookup"><span data-stu-id="3ee6d-189">2</span></span>
- <span data-ttu-id="3ee6d-190">3,2</span><span class="sxs-lookup"><span data-stu-id="3ee6d-190">3</span></span>
- <span data-ttu-id="3ee6d-191">r.[4</span><span class="sxs-lookup"><span data-stu-id="3ee6d-191">4</span></span>
- <span data-ttu-id="3ee6d-192">art</span><span class="sxs-lookup"><span data-stu-id="3ee6d-192">5</span></span>
- <span data-ttu-id="3ee6d-193">2,6</span><span class="sxs-lookup"><span data-stu-id="3ee6d-193">6</span></span>
- <span data-ttu-id="3ee6d-194">7,3</span><span class="sxs-lookup"><span data-stu-id="3ee6d-194">7</span></span>
- <span data-ttu-id="3ee6d-195">8</span><span class="sxs-lookup"><span data-stu-id="3ee6d-195">8</span></span>
- <span data-ttu-id="3ee6d-196">9</span><span class="sxs-lookup"><span data-stu-id="3ee6d-196">9</span></span> 
- <span data-ttu-id="3ee6d-197">dziesięciu</span><span class="sxs-lookup"><span data-stu-id="3ee6d-197">10</span></span>

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

### <span data-ttu-id="3ee6d-198">-Size</span><span class="sxs-lookup"><span data-stu-id="3ee6d-198">-Size</span></span>
<span data-ttu-id="3ee6d-199">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="3ee6d-200">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-200">Valid values are:</span></span> 

- <span data-ttu-id="3ee6d-201">Punkt</span><span class="sxs-lookup"><span data-stu-id="3ee6d-201">P1</span></span>
- <span data-ttu-id="3ee6d-202">Punktu</span><span class="sxs-lookup"><span data-stu-id="3ee6d-202">P2</span></span>
- <span data-ttu-id="3ee6d-203">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="3ee6d-203">P3</span></span>
- <span data-ttu-id="3ee6d-204">P4</span><span class="sxs-lookup"><span data-stu-id="3ee6d-204">P4</span></span>
- <span data-ttu-id="3ee6d-205">C0</span><span class="sxs-lookup"><span data-stu-id="3ee6d-205">C0</span></span>
- <span data-ttu-id="3ee6d-206">C1</span><span class="sxs-lookup"><span data-stu-id="3ee6d-206">C1</span></span>
- <span data-ttu-id="3ee6d-207">C2</span><span class="sxs-lookup"><span data-stu-id="3ee6d-207">C2</span></span>
- <span data-ttu-id="3ee6d-208">C3</span><span class="sxs-lookup"><span data-stu-id="3ee6d-208">C3</span></span>
- <span data-ttu-id="3ee6d-209">C4</span><span class="sxs-lookup"><span data-stu-id="3ee6d-209">C4</span></span>
- <span data-ttu-id="3ee6d-210">C5</span><span class="sxs-lookup"><span data-stu-id="3ee6d-210">C5</span></span>
- <span data-ttu-id="3ee6d-211">C6</span><span class="sxs-lookup"><span data-stu-id="3ee6d-211">C6</span></span>
- <span data-ttu-id="3ee6d-212">250MB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-212">250MB</span></span>
- <span data-ttu-id="3ee6d-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-213">1GB</span></span>
- <span data-ttu-id="3ee6d-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-214">2.5GB</span></span>
- <span data-ttu-id="3ee6d-215">6GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-215">6GB</span></span>
- <span data-ttu-id="3ee6d-216">13GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-216">13GB</span></span>
- <span data-ttu-id="3ee6d-217">26GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-217">26GB</span></span>
- <span data-ttu-id="3ee6d-218">53GB</span><span class="sxs-lookup"><span data-stu-id="3ee6d-218">53GB</span></span>

<span data-ttu-id="3ee6d-219">Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="3ee6d-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="3ee6d-220">-Sku</span></span>
<span data-ttu-id="3ee6d-221">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="3ee6d-222">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ee6d-222">Valid values are:</span></span> 

- <span data-ttu-id="3ee6d-223">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3ee6d-223">Basic</span></span>
- <span data-ttu-id="3ee6d-224">Standard</span><span class="sxs-lookup"><span data-stu-id="3ee6d-224">Standard</span></span>
- <span data-ttu-id="3ee6d-225">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="3ee6d-225">Premium</span></span>

<span data-ttu-id="3ee6d-226">Wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="3ee6d-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="3ee6d-227">-StaticIP</span></span>
<span data-ttu-id="3ee6d-228">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="3ee6d-229">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="3ee6d-230">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="3ee6d-230">-Subnet</span></span>
<span data-ttu-id="3ee6d-231">Określa nazwę podsieci, w której ma zostać wdrożona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="3ee6d-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3ee6d-232">-SubnetId</span></span>
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

### <span data-ttu-id="3ee6d-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="3ee6d-233">-TenantSettings</span></span>
<span data-ttu-id="3ee6d-234">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="3ee6d-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ee6d-235">-VirtualNetwork</span></span>
<span data-ttu-id="3ee6d-236">Określa identyfikator zasobu sieci wirtualnej, w którym ma zostać wdrożona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="3ee6d-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee6d-237">-DefaultProfile</span></span>
<span data-ttu-id="3ee6d-238">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee6d-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee6d-239">CommonParameters</span></span>
<span data-ttu-id="3ee6d-240">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee6d-241">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee6d-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee6d-242">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ee6d-242">INPUTS</span></span>

### <span data-ttu-id="3ee6d-243">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3ee6d-243">None</span></span>
<span data-ttu-id="3ee6d-244">Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="3ee6d-245">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ee6d-245">OUTPUTS</span></span>

### <span data-ttu-id="3ee6d-246">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3ee6d-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="3ee6d-247">To polecenie cmdlet zwraca wszystkie atrybuty pamięci podręcznej Redis, w tym klucze podstawowych i pomocniczych dostępu.</span><span class="sxs-lookup"><span data-stu-id="3ee6d-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="3ee6d-248">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ee6d-248">NOTES</span></span>

## <span data-ttu-id="3ee6d-249">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ee6d-249">RELATED LINKS</span></span>

[<span data-ttu-id="3ee6d-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3ee6d-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="3ee6d-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3ee6d-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="3ee6d-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3ee6d-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


