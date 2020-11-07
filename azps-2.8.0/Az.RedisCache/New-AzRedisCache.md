---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872552"
---
# <span data-ttu-id="dab4a-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dab4a-101">New-AzRedisCache</span></span>

## <span data-ttu-id="dab4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dab4a-102">SYNOPSIS</span></span>
<span data-ttu-id="dab4a-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="dab4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dab4a-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dab4a-105">DESCRIPTION</span></span>
<span data-ttu-id="dab4a-106">Polecenie cmdlet **New-AzRedisCache** tworzy pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="dab4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dab4a-107">EXAMPLES</span></span>

### <span data-ttu-id="dab4a-108">Przykład 1. tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="dab4a-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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

<span data-ttu-id="dab4a-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="dab4a-110">Przykład 2: Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="dab4a-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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

<span data-ttu-id="dab4a-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="dab4a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dab4a-112">PARAMETERS</span></span>

### <span data-ttu-id="dab4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab4a-113">-DefaultProfile</span></span>
<span data-ttu-id="dab4a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dab4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab4a-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dab4a-115">-EnableNonSslPort</span></span>
<span data-ttu-id="dab4a-116">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="dab4a-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dab4a-117">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="dab4a-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dab4a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dab4a-118">-Location</span></span>
<span data-ttu-id="dab4a-119">Określa lokalizację, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="dab4a-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="dab4a-120">Valid values are:</span></span> 
- <span data-ttu-id="dab4a-121">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="dab4a-121">North Central US</span></span>
- <span data-ttu-id="dab4a-122">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="dab4a-122">South Central US</span></span>
- <span data-ttu-id="dab4a-123">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="dab4a-123">Central US</span></span>
- <span data-ttu-id="dab4a-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="dab4a-124">West Europe</span></span>
- <span data-ttu-id="dab4a-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="dab4a-125">North Europe</span></span>
- <span data-ttu-id="dab4a-126">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="dab4a-126">West US</span></span>
- <span data-ttu-id="dab4a-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="dab4a-127">East US</span></span>
- <span data-ttu-id="dab4a-128">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="dab4a-128">East US 2</span></span>
- <span data-ttu-id="dab4a-129">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="dab4a-129">Japan East</span></span>
- <span data-ttu-id="dab4a-130">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="dab4a-130">Japan West</span></span>
- <span data-ttu-id="dab4a-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="dab4a-131">Brazil South</span></span>
- <span data-ttu-id="dab4a-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="dab4a-132">Southeast Asia</span></span>
- <span data-ttu-id="dab4a-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="dab4a-133">East Asia</span></span>
- <span data-ttu-id="dab4a-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="dab4a-134">Australia East</span></span>
- <span data-ttu-id="dab4a-135">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="dab4a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="dab4a-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dab4a-136">-Name</span></span>
<span data-ttu-id="dab4a-137">Określa nazwę pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="dab4a-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="dab4a-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dab4a-138">-RedisConfiguration</span></span>
<span data-ttu-id="dab4a-139">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dab4a-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dab4a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dab4a-141">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="dab4a-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="dab4a-142">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="dab4a-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dab4a-143">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-143">Premium tier only.</span></span>
- <span data-ttu-id="dab4a-144">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="dab4a-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dab4a-145">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="dab4a-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dab4a-146">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-146">Premium tier only.</span></span>
- <span data-ttu-id="dab4a-147">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="dab4a-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="dab4a-148">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="dab4a-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dab4a-149">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-149">Premium tier only.</span></span> 
- <span data-ttu-id="dab4a-150">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="dab4a-150">maxmemory-reserved.</span></span>
<span data-ttu-id="dab4a-151">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="dab4a-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dab4a-152">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-153">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="dab4a-153">maxmemory-policy.</span></span>
<span data-ttu-id="dab4a-154">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="dab4a-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dab4a-155">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="dab4a-155">All pricing tiers.</span></span> 
- <span data-ttu-id="dab4a-156">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="dab4a-156">notify-keyspace-events.</span></span>
<span data-ttu-id="dab4a-157">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="dab4a-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="dab4a-158">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dab4a-159">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="dab4a-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dab4a-160">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="dab4a-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dab4a-161">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-162">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="dab4a-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dab4a-163">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="dab4a-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dab4a-164">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-165">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="dab4a-165">set-max-intset-entries.</span></span>
<span data-ttu-id="dab4a-166">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="dab4a-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dab4a-167">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-168">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="dab4a-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dab4a-169">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="dab4a-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dab4a-170">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-171">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="dab4a-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dab4a-172">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="dab4a-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dab4a-173">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dab4a-174">baz danych.</span><span class="sxs-lookup"><span data-stu-id="dab4a-174">databases.</span></span>
<span data-ttu-id="dab4a-175">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="dab4a-175">Configures the number of databases.</span></span>
<span data-ttu-id="dab4a-176">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="dab4a-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dab4a-177">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="dab4a-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="dab4a-178">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dab4a-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dab4a-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab4a-179">-ResourceGroupName</span></span>
<span data-ttu-id="dab4a-180">Określa nazwę grupy zasobów, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="dab4a-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dab4a-181">-ShardCount</span></span>
<span data-ttu-id="dab4a-182">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="dab4a-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="dab4a-183">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dab4a-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dab4a-184">jedno</span><span class="sxs-lookup"><span data-stu-id="dab4a-184">1</span></span>
- <span data-ttu-id="dab4a-185">2,6</span><span class="sxs-lookup"><span data-stu-id="dab4a-185">2</span></span>
- <span data-ttu-id="dab4a-186">3,2</span><span class="sxs-lookup"><span data-stu-id="dab4a-186">3</span></span>
- <span data-ttu-id="dab4a-187">r.[4</span><span class="sxs-lookup"><span data-stu-id="dab4a-187">4</span></span>
- <span data-ttu-id="dab4a-188">art</span><span class="sxs-lookup"><span data-stu-id="dab4a-188">5</span></span>
- <span data-ttu-id="dab4a-189">2,6</span><span class="sxs-lookup"><span data-stu-id="dab4a-189">6</span></span>
- <span data-ttu-id="dab4a-190">7,3</span><span class="sxs-lookup"><span data-stu-id="dab4a-190">7</span></span>
- <span data-ttu-id="dab4a-191">8</span><span class="sxs-lookup"><span data-stu-id="dab4a-191">8</span></span>
- <span data-ttu-id="dab4a-192">9</span><span class="sxs-lookup"><span data-stu-id="dab4a-192">9</span></span> 
- <span data-ttu-id="dab4a-193">dziesięciu</span><span class="sxs-lookup"><span data-stu-id="dab4a-193">10</span></span>

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

### <span data-ttu-id="dab4a-194">-Size</span><span class="sxs-lookup"><span data-stu-id="dab4a-194">-Size</span></span>
<span data-ttu-id="dab4a-195">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dab4a-196">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="dab4a-196">Valid values are:</span></span> 
- <span data-ttu-id="dab4a-197">Punkt</span><span class="sxs-lookup"><span data-stu-id="dab4a-197">P1</span></span>
- <span data-ttu-id="dab4a-198">Punktu</span><span class="sxs-lookup"><span data-stu-id="dab4a-198">P2</span></span>
- <span data-ttu-id="dab4a-199">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="dab4a-199">P3</span></span>
- <span data-ttu-id="dab4a-200">P4</span><span class="sxs-lookup"><span data-stu-id="dab4a-200">P4</span></span>
- <span data-ttu-id="dab4a-201">C0</span><span class="sxs-lookup"><span data-stu-id="dab4a-201">C0</span></span>
- <span data-ttu-id="dab4a-202">C1</span><span class="sxs-lookup"><span data-stu-id="dab4a-202">C1</span></span>
- <span data-ttu-id="dab4a-203">C2</span><span class="sxs-lookup"><span data-stu-id="dab4a-203">C2</span></span>
- <span data-ttu-id="dab4a-204">C3</span><span class="sxs-lookup"><span data-stu-id="dab4a-204">C3</span></span>
- <span data-ttu-id="dab4a-205">C4</span><span class="sxs-lookup"><span data-stu-id="dab4a-205">C4</span></span>
- <span data-ttu-id="dab4a-206">C5</span><span class="sxs-lookup"><span data-stu-id="dab4a-206">C5</span></span>
- <span data-ttu-id="dab4a-207">C6</span><span class="sxs-lookup"><span data-stu-id="dab4a-207">C6</span></span>
- <span data-ttu-id="dab4a-208">250MB</span><span class="sxs-lookup"><span data-stu-id="dab4a-208">250MB</span></span>
- <span data-ttu-id="dab4a-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="dab4a-209">1GB</span></span>
- <span data-ttu-id="dab4a-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="dab4a-210">2.5GB</span></span>
- <span data-ttu-id="dab4a-211">6GB</span><span class="sxs-lookup"><span data-stu-id="dab4a-211">6GB</span></span>
- <span data-ttu-id="dab4a-212">13GB</span><span class="sxs-lookup"><span data-stu-id="dab4a-212">13GB</span></span>
- <span data-ttu-id="dab4a-213">26GB</span><span class="sxs-lookup"><span data-stu-id="dab4a-213">26GB</span></span>
- <span data-ttu-id="dab4a-214">53GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="dab4a-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dab4a-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="dab4a-215">-Sku</span></span>
<span data-ttu-id="dab4a-216">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="dab4a-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dab4a-217">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="dab4a-217">Valid values are:</span></span> 
- <span data-ttu-id="dab4a-218">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="dab4a-218">Basic</span></span>
- <span data-ttu-id="dab4a-219">Standard</span><span class="sxs-lookup"><span data-stu-id="dab4a-219">Standard</span></span>
- <span data-ttu-id="dab4a-220">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="dab4a-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="dab4a-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="dab4a-221">-StaticIP</span></span>
<span data-ttu-id="dab4a-222">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="dab4a-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="dab4a-223">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="dab4a-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="dab4a-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dab4a-224">-SubnetId</span></span>
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

### <span data-ttu-id="dab4a-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="dab4a-225">-Tag</span></span>
<span data-ttu-id="dab4a-226">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="dab4a-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="dab4a-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dab4a-227">-TenantSettings</span></span>
<span data-ttu-id="dab4a-228">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="dab4a-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dab4a-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="dab4a-229">-Zone</span></span>
<span data-ttu-id="dab4a-230">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="dab4a-230">List of zones.</span></span>

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

### <span data-ttu-id="dab4a-231">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dab4a-231">-Confirm</span></span>
<span data-ttu-id="dab4a-232">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dab4a-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab4a-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab4a-233">-WhatIf</span></span>
<span data-ttu-id="dab4a-234">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dab4a-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dab4a-235">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dab4a-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab4a-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab4a-236">CommonParameters</span></span>
<span data-ttu-id="dab4a-237">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dab4a-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab4a-238">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab4a-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab4a-239">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dab4a-239">INPUTS</span></span>

### <span data-ttu-id="dab4a-240">System. String</span><span class="sxs-lookup"><span data-stu-id="dab4a-240">System.String</span></span>

### <span data-ttu-id="dab4a-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dab4a-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dab4a-242">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dab4a-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dab4a-243">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dab4a-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dab4a-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="dab4a-244">System.String[]</span></span>

## <span data-ttu-id="dab4a-245">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dab4a-245">OUTPUTS</span></span>

### <span data-ttu-id="dab4a-246">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dab4a-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="dab4a-247">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dab4a-247">NOTES</span></span>

## <span data-ttu-id="dab4a-248">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dab4a-248">RELATED LINKS</span></span>

[<span data-ttu-id="dab4a-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dab4a-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dab4a-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dab4a-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dab4a-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dab4a-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


