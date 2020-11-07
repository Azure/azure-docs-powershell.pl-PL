---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717911"
---
# <span data-ttu-id="424d4-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="424d4-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="424d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="424d4-102">SYNOPSIS</span></span>
<span data-ttu-id="424d4-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="424d4-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="424d4-105">DESCRIPTION</span></span>
<span data-ttu-id="424d4-106">Polecenie cmdlet **New-AzureRmRedisCache** tworzy pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="424d4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="424d4-107">EXAMPLES</span></span>

### <span data-ttu-id="424d4-108">Przykład 1. tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="424d4-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="424d4-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="424d4-110">Przykład 2: Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="424d4-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="424d4-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="424d4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="424d4-112">PARAMETERS</span></span>

### <span data-ttu-id="424d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424d4-113">-DefaultProfile</span></span>
<span data-ttu-id="424d4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="424d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424d4-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="424d4-115">-EnableNonSslPort</span></span>
<span data-ttu-id="424d4-116">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="424d4-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="424d4-117">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="424d4-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="424d4-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="424d4-118">-Location</span></span>
<span data-ttu-id="424d4-119">Określa lokalizację, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="424d4-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="424d4-120">Valid values are:</span></span> 
- <span data-ttu-id="424d4-121">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="424d4-121">North Central US</span></span>
- <span data-ttu-id="424d4-122">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="424d4-122">South Central US</span></span>
- <span data-ttu-id="424d4-123">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="424d4-123">Central US</span></span>
- <span data-ttu-id="424d4-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="424d4-124">West Europe</span></span>
- <span data-ttu-id="424d4-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="424d4-125">North Europe</span></span>
- <span data-ttu-id="424d4-126">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="424d4-126">West US</span></span>
- <span data-ttu-id="424d4-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="424d4-127">East US</span></span>
- <span data-ttu-id="424d4-128">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="424d4-128">East US 2</span></span>
- <span data-ttu-id="424d4-129">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="424d4-129">Japan East</span></span>
- <span data-ttu-id="424d4-130">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="424d4-130">Japan West</span></span>
- <span data-ttu-id="424d4-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="424d4-131">Brazil South</span></span>
- <span data-ttu-id="424d4-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="424d4-132">Southeast Asia</span></span>
- <span data-ttu-id="424d4-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="424d4-133">East Asia</span></span>
- <span data-ttu-id="424d4-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="424d4-134">Australia East</span></span>
- <span data-ttu-id="424d4-135">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="424d4-135">Australia Southeast</span></span>

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

### <span data-ttu-id="424d4-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="424d4-136">-Name</span></span>
<span data-ttu-id="424d4-137">Określa nazwę pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="424d4-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="424d4-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="424d4-138">-RedisConfiguration</span></span>
<span data-ttu-id="424d4-139">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="424d4-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="424d4-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="424d4-141">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="424d4-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="424d4-142">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="424d4-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="424d4-143">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-143">Premium tier only.</span></span>
- <span data-ttu-id="424d4-144">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="424d4-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="424d4-145">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="424d4-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="424d4-146">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-146">Premium tier only.</span></span>
- <span data-ttu-id="424d4-147">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="424d4-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="424d4-148">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="424d4-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="424d4-149">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-149">Premium tier only.</span></span> 
- <span data-ttu-id="424d4-150">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="424d4-150">maxmemory-reserved.</span></span>
<span data-ttu-id="424d4-151">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="424d4-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="424d4-152">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-153">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="424d4-153">maxmemory-policy.</span></span>
<span data-ttu-id="424d4-154">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="424d4-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="424d4-155">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="424d4-155">All pricing tiers.</span></span> 
- <span data-ttu-id="424d4-156">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="424d4-156">notify-keyspace-events.</span></span>
<span data-ttu-id="424d4-157">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="424d4-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="424d4-158">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="424d4-159">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="424d4-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="424d4-160">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="424d4-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="424d4-161">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-162">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="424d4-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="424d4-163">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="424d4-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="424d4-164">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-165">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="424d4-165">set-max-intset-entries.</span></span>
<span data-ttu-id="424d4-166">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="424d4-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="424d4-167">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-168">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="424d4-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="424d4-169">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="424d4-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="424d4-170">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-171">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="424d4-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="424d4-172">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="424d4-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="424d4-173">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="424d4-174">baz danych.</span><span class="sxs-lookup"><span data-stu-id="424d4-174">databases.</span></span>
<span data-ttu-id="424d4-175">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="424d4-175">Configures the number of databases.</span></span>
<span data-ttu-id="424d4-176">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="424d4-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="424d4-177">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="424d4-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="424d4-178">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="424d4-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="424d4-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424d4-179">-ResourceGroupName</span></span>
<span data-ttu-id="424d4-180">Określa nazwę grupy zasobów, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="424d4-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="424d4-181">-ShardCount</span></span>
<span data-ttu-id="424d4-182">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="424d4-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="424d4-183">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="424d4-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="424d4-184">jedno</span><span class="sxs-lookup"><span data-stu-id="424d4-184">1</span></span>
- <span data-ttu-id="424d4-185">2,6</span><span class="sxs-lookup"><span data-stu-id="424d4-185">2</span></span>
- <span data-ttu-id="424d4-186">3,2</span><span class="sxs-lookup"><span data-stu-id="424d4-186">3</span></span>
- <span data-ttu-id="424d4-187">r.[4</span><span class="sxs-lookup"><span data-stu-id="424d4-187">4</span></span>
- <span data-ttu-id="424d4-188">art</span><span class="sxs-lookup"><span data-stu-id="424d4-188">5</span></span>
- <span data-ttu-id="424d4-189">2,6</span><span class="sxs-lookup"><span data-stu-id="424d4-189">6</span></span>
- <span data-ttu-id="424d4-190">7,3</span><span class="sxs-lookup"><span data-stu-id="424d4-190">7</span></span>
- <span data-ttu-id="424d4-191">8</span><span class="sxs-lookup"><span data-stu-id="424d4-191">8</span></span>
- <span data-ttu-id="424d4-192">9</span><span class="sxs-lookup"><span data-stu-id="424d4-192">9</span></span> 
- <span data-ttu-id="424d4-193">dziesięciu</span><span class="sxs-lookup"><span data-stu-id="424d4-193">10</span></span>

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

### <span data-ttu-id="424d4-194">-Size</span><span class="sxs-lookup"><span data-stu-id="424d4-194">-Size</span></span>
<span data-ttu-id="424d4-195">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="424d4-196">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="424d4-196">Valid values are:</span></span> 
- <span data-ttu-id="424d4-197">Punkt</span><span class="sxs-lookup"><span data-stu-id="424d4-197">P1</span></span>
- <span data-ttu-id="424d4-198">Punktu</span><span class="sxs-lookup"><span data-stu-id="424d4-198">P2</span></span>
- <span data-ttu-id="424d4-199">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="424d4-199">P3</span></span>
- <span data-ttu-id="424d4-200">P4</span><span class="sxs-lookup"><span data-stu-id="424d4-200">P4</span></span>
- <span data-ttu-id="424d4-201">C0</span><span class="sxs-lookup"><span data-stu-id="424d4-201">C0</span></span>
- <span data-ttu-id="424d4-202">C1</span><span class="sxs-lookup"><span data-stu-id="424d4-202">C1</span></span>
- <span data-ttu-id="424d4-203">C2</span><span class="sxs-lookup"><span data-stu-id="424d4-203">C2</span></span>
- <span data-ttu-id="424d4-204">C3</span><span class="sxs-lookup"><span data-stu-id="424d4-204">C3</span></span>
- <span data-ttu-id="424d4-205">C4</span><span class="sxs-lookup"><span data-stu-id="424d4-205">C4</span></span>
- <span data-ttu-id="424d4-206">C5</span><span class="sxs-lookup"><span data-stu-id="424d4-206">C5</span></span>
- <span data-ttu-id="424d4-207">C6</span><span class="sxs-lookup"><span data-stu-id="424d4-207">C6</span></span>
- <span data-ttu-id="424d4-208">250MB</span><span class="sxs-lookup"><span data-stu-id="424d4-208">250MB</span></span>
- <span data-ttu-id="424d4-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="424d4-209">1GB</span></span>
- <span data-ttu-id="424d4-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="424d4-210">2.5GB</span></span>
- <span data-ttu-id="424d4-211">6GB</span><span class="sxs-lookup"><span data-stu-id="424d4-211">6GB</span></span>
- <span data-ttu-id="424d4-212">13GB</span><span class="sxs-lookup"><span data-stu-id="424d4-212">13GB</span></span>
- <span data-ttu-id="424d4-213">26GB</span><span class="sxs-lookup"><span data-stu-id="424d4-213">26GB</span></span>
- <span data-ttu-id="424d4-214">53GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="424d4-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="424d4-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="424d4-215">-Sku</span></span>
<span data-ttu-id="424d4-216">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="424d4-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="424d4-217">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="424d4-217">Valid values are:</span></span> 
- <span data-ttu-id="424d4-218">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="424d4-218">Basic</span></span>
- <span data-ttu-id="424d4-219">Standard</span><span class="sxs-lookup"><span data-stu-id="424d4-219">Standard</span></span>
- <span data-ttu-id="424d4-220">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="424d4-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="424d4-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="424d4-221">-StaticIP</span></span>
<span data-ttu-id="424d4-222">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="424d4-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="424d4-223">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="424d4-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="424d4-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="424d4-224">-SubnetId</span></span>
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

### <span data-ttu-id="424d4-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="424d4-225">-Tag</span></span>
<span data-ttu-id="424d4-226">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="424d4-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="424d4-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="424d4-227">-TenantSettings</span></span>
<span data-ttu-id="424d4-228">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="424d4-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="424d4-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="424d4-229">-Zone</span></span>
<span data-ttu-id="424d4-230">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="424d4-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424d4-231">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="424d4-231">-Confirm</span></span>
<span data-ttu-id="424d4-232">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d4-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424d4-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424d4-233">-WhatIf</span></span>
<span data-ttu-id="424d4-234">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d4-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="424d4-235">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="424d4-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424d4-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424d4-236">CommonParameters</span></span>
<span data-ttu-id="424d4-237">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424d4-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424d4-238">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424d4-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424d4-239">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424d4-239">INPUTS</span></span>

### <span data-ttu-id="424d4-240">System. String</span><span class="sxs-lookup"><span data-stu-id="424d4-240">System.String</span></span>

### <span data-ttu-id="424d4-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="424d4-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="424d4-242">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="424d4-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="424d4-243">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="424d4-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="424d4-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="424d4-244">System.String[]</span></span>

## <span data-ttu-id="424d4-245">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="424d4-245">OUTPUTS</span></span>

### <span data-ttu-id="424d4-246">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="424d4-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="424d4-247">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="424d4-247">NOTES</span></span>

## <span data-ttu-id="424d4-248">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="424d4-248">RELATED LINKS</span></span>

[<span data-ttu-id="424d4-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="424d4-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="424d4-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="424d4-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="424d4-251">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="424d4-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


