---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542388"
---
# <span data-ttu-id="d9c4f-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9c4f-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="d9c4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c4f-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9c4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9c4f-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c4f-106">Polecenie cmdlet **New-AzureRmRedisCache** tworzy pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d9c4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c4f-108">Przykład 1. tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="d9c4f-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="d9c4f-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d9c4f-110">Przykład 2: Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="d9c4f-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="d9c4f-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d9c4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9c4f-112">PARAMETERS</span></span>

### <span data-ttu-id="d9c4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c4f-113">-DefaultProfile</span></span>
<span data-ttu-id="d9c4f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c4f-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d9c4f-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d9c4f-116">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d9c4f-117">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="d9c4f-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d9c4f-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9c4f-118">-Location</span></span>
<span data-ttu-id="d9c4f-119">Określa lokalizację, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d9c4f-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-120">Valid values are:</span></span> 

- <span data-ttu-id="d9c4f-121">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="d9c4f-121">North Central US</span></span>
- <span data-ttu-id="d9c4f-122">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="d9c4f-122">South Central US</span></span>
- <span data-ttu-id="d9c4f-123">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="d9c4f-123">Central US</span></span>
- <span data-ttu-id="d9c4f-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="d9c4f-124">West Europe</span></span>
- <span data-ttu-id="d9c4f-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="d9c4f-125">North Europe</span></span>
- <span data-ttu-id="d9c4f-126">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="d9c4f-126">West US</span></span>
- <span data-ttu-id="d9c4f-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="d9c4f-127">East US</span></span>
- <span data-ttu-id="d9c4f-128">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="d9c4f-128">East US 2</span></span>
- <span data-ttu-id="d9c4f-129">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="d9c4f-129">Japan East</span></span>
- <span data-ttu-id="d9c4f-130">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="d9c4f-130">Japan West</span></span>
- <span data-ttu-id="d9c4f-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="d9c4f-131">Brazil South</span></span>
- <span data-ttu-id="d9c4f-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d9c4f-132">Southeast Asia</span></span>
- <span data-ttu-id="d9c4f-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d9c4f-133">East Asia</span></span>
- <span data-ttu-id="d9c4f-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d9c4f-134">Australia East</span></span>
- <span data-ttu-id="d9c4f-135">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="d9c4f-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d9c4f-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="d9c4f-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="d9c4f-137">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="d9c4f-138">Użyj parametru *RedisConfiguration* , aby ustawić maxmemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="d9c4f-139">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-139">For example:</span></span> 

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

### <span data-ttu-id="d9c4f-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9c4f-140">-Name</span></span>
<span data-ttu-id="d9c4f-141">Określa nazwę pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d9c4f-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9c4f-142">-RedisConfiguration</span></span>
<span data-ttu-id="d9c4f-143">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d9c4f-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9c4f-145">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="d9c4f-146">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d9c4f-147">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-147">Premium tier only.</span></span>
- <span data-ttu-id="d9c4f-148">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="d9c4f-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d9c4f-149">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d9c4f-150">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-150">Premium tier only.</span></span>
- <span data-ttu-id="d9c4f-151">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="d9c4f-152">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d9c4f-153">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-153">Premium tier only.</span></span> 
- <span data-ttu-id="d9c4f-154">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-154">maxmemory-reserved.</span></span>
<span data-ttu-id="d9c4f-155">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d9c4f-156">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-157">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-157">maxmemory-policy.</span></span>
<span data-ttu-id="d9c4f-158">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d9c4f-159">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-159">All pricing tiers.</span></span> 
- <span data-ttu-id="d9c4f-160">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-160">notify-keyspace-events.</span></span>
<span data-ttu-id="d9c4f-161">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="d9c4f-162">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-163">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d9c4f-164">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d9c4f-165">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-166">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d9c4f-167">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d9c4f-168">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-169">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-169">set-max-intset-entries.</span></span>
<span data-ttu-id="d9c4f-170">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d9c4f-171">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-172">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d9c4f-173">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d9c4f-174">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-175">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d9c4f-176">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d9c4f-177">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d9c4f-178">baz danych.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-178">databases.</span></span>
<span data-ttu-id="d9c4f-179">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-179">Configures the number of databases.</span></span>
<span data-ttu-id="d9c4f-180">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d9c4f-181">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="d9c4f-182">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="d9c4f-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d9c4f-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="d9c4f-183">-RedisVersion</span></span>
<span data-ttu-id="d9c4f-184">Ten parametr jest przestarzały i zostanie usunięty z przyszłych wersji.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="d9c4f-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c4f-185">-ResourceGroupName</span></span>
<span data-ttu-id="d9c4f-186">Określa nazwę grupy zasobów, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d9c4f-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d9c4f-187">-ShardCount</span></span>
<span data-ttu-id="d9c4f-188">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d9c4f-189">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9c4f-190">jedno</span><span class="sxs-lookup"><span data-stu-id="d9c4f-190">1</span></span>
- <span data-ttu-id="d9c4f-191">2,6</span><span class="sxs-lookup"><span data-stu-id="d9c4f-191">2</span></span>
- <span data-ttu-id="d9c4f-192">3,2</span><span class="sxs-lookup"><span data-stu-id="d9c4f-192">3</span></span>
- <span data-ttu-id="d9c4f-193">r.[4</span><span class="sxs-lookup"><span data-stu-id="d9c4f-193">4</span></span>
- <span data-ttu-id="d9c4f-194">art</span><span class="sxs-lookup"><span data-stu-id="d9c4f-194">5</span></span>
- <span data-ttu-id="d9c4f-195">2,6</span><span class="sxs-lookup"><span data-stu-id="d9c4f-195">6</span></span>
- <span data-ttu-id="d9c4f-196">7,3</span><span class="sxs-lookup"><span data-stu-id="d9c4f-196">7</span></span>
- <span data-ttu-id="d9c4f-197">8</span><span class="sxs-lookup"><span data-stu-id="d9c4f-197">8</span></span>
- <span data-ttu-id="d9c4f-198">9</span><span class="sxs-lookup"><span data-stu-id="d9c4f-198">9</span></span> 
- <span data-ttu-id="d9c4f-199">dziesięciu</span><span class="sxs-lookup"><span data-stu-id="d9c4f-199">10</span></span>

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

### <span data-ttu-id="d9c4f-200">-Size</span><span class="sxs-lookup"><span data-stu-id="d9c4f-200">-Size</span></span>
<span data-ttu-id="d9c4f-201">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d9c4f-202">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-202">Valid values are:</span></span> 

- <span data-ttu-id="d9c4f-203">Punkt</span><span class="sxs-lookup"><span data-stu-id="d9c4f-203">P1</span></span>
- <span data-ttu-id="d9c4f-204">Punktu</span><span class="sxs-lookup"><span data-stu-id="d9c4f-204">P2</span></span>
- <span data-ttu-id="d9c4f-205">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="d9c4f-205">P3</span></span>
- <span data-ttu-id="d9c4f-206">P4</span><span class="sxs-lookup"><span data-stu-id="d9c4f-206">P4</span></span>
- <span data-ttu-id="d9c4f-207">C0</span><span class="sxs-lookup"><span data-stu-id="d9c4f-207">C0</span></span>
- <span data-ttu-id="d9c4f-208">C1</span><span class="sxs-lookup"><span data-stu-id="d9c4f-208">C1</span></span>
- <span data-ttu-id="d9c4f-209">C2</span><span class="sxs-lookup"><span data-stu-id="d9c4f-209">C2</span></span>
- <span data-ttu-id="d9c4f-210">C3</span><span class="sxs-lookup"><span data-stu-id="d9c4f-210">C3</span></span>
- <span data-ttu-id="d9c4f-211">C4</span><span class="sxs-lookup"><span data-stu-id="d9c4f-211">C4</span></span>
- <span data-ttu-id="d9c4f-212">C5</span><span class="sxs-lookup"><span data-stu-id="d9c4f-212">C5</span></span>
- <span data-ttu-id="d9c4f-213">C6</span><span class="sxs-lookup"><span data-stu-id="d9c4f-213">C6</span></span>
- <span data-ttu-id="d9c4f-214">250MB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-214">250MB</span></span>
- <span data-ttu-id="d9c4f-215">1 GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-215">1GB</span></span>
- <span data-ttu-id="d9c4f-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-216">2.5GB</span></span>
- <span data-ttu-id="d9c4f-217">6GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-217">6GB</span></span>
- <span data-ttu-id="d9c4f-218">13GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-218">13GB</span></span>
- <span data-ttu-id="d9c4f-219">26GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-219">26GB</span></span>
- <span data-ttu-id="d9c4f-220">53GB</span><span class="sxs-lookup"><span data-stu-id="d9c4f-220">53GB</span></span>

<span data-ttu-id="d9c4f-221">Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d9c4f-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="d9c4f-222">-Sku</span></span>
<span data-ttu-id="d9c4f-223">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d9c4f-224">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d9c4f-224">Valid values are:</span></span> 

- <span data-ttu-id="d9c4f-225">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="d9c4f-225">Basic</span></span>
- <span data-ttu-id="d9c4f-226">Standard</span><span class="sxs-lookup"><span data-stu-id="d9c4f-226">Standard</span></span>
- <span data-ttu-id="d9c4f-227">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="d9c4f-227">Premium</span></span>

<span data-ttu-id="d9c4f-228">Wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="d9c4f-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d9c4f-229">-StaticIP</span></span>
<span data-ttu-id="d9c4f-230">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="d9c4f-231">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d9c4f-232">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="d9c4f-232">-Subnet</span></span>
<span data-ttu-id="d9c4f-233">Określa nazwę podsieci, w której ma zostać wdrożona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d9c4f-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d9c4f-234">-SubnetId</span></span>
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

### <span data-ttu-id="d9c4f-235">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9c4f-235">-Tag</span></span>
<span data-ttu-id="d9c4f-236">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d9c4f-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d9c4f-237">-TenantSettings</span></span>
<span data-ttu-id="d9c4f-238">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d9c4f-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c4f-239">-VirtualNetwork</span></span>
<span data-ttu-id="d9c4f-240">Określa identyfikator zasobu sieci wirtualnej, w którym ma zostać wdrożona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d9c4f-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="d9c4f-241">-Zone</span></span>
<span data-ttu-id="d9c4f-242">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c4f-243">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9c4f-243">-Confirm</span></span>
<span data-ttu-id="d9c4f-244">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c4f-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c4f-245">-WhatIf</span></span>
<span data-ttu-id="d9c4f-246">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9c4f-247">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c4f-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c4f-248">CommonParameters</span></span>
<span data-ttu-id="d9c4f-249">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c4f-250">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c4f-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c4f-251">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9c4f-251">INPUTS</span></span>

### <span data-ttu-id="d9c4f-252">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9c4f-252">None</span></span>
<span data-ttu-id="d9c4f-253">Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d9c4f-254">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9c4f-254">OUTPUTS</span></span>

### <span data-ttu-id="d9c4f-255">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d9c4f-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="d9c4f-256">To polecenie cmdlet zwraca wszystkie atrybuty pamięci podręcznej Redis, w tym klucze podstawowych i pomocniczych dostępu.</span><span class="sxs-lookup"><span data-stu-id="d9c4f-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="d9c4f-257">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9c4f-257">NOTES</span></span>

## <span data-ttu-id="d9c4f-258">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9c4f-258">RELATED LINKS</span></span>

[<span data-ttu-id="d9c4f-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9c4f-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d9c4f-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9c4f-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d9c4f-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9c4f-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


