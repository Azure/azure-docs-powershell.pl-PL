---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490741"
---
# <span data-ttu-id="4ae1b-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ae1b-101">New-AzRedisCache</span></span>

## <span data-ttu-id="4ae1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ae1b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae1b-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="4ae1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ae1b-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ae1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ae1b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae1b-106">Polecenie cmdlet **New-AzRedisCache** tworzy pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="4ae1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ae1b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae1b-108">Przykład 1. tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="4ae1b-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="4ae1b-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="4ae1b-110">Przykład 2: Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="4ae1b-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="4ae1b-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="4ae1b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ae1b-112">PARAMETERS</span></span>

### <span data-ttu-id="4ae1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae1b-113">-DefaultProfile</span></span>
<span data-ttu-id="4ae1b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae1b-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="4ae1b-115">-EnableNonSslPort</span></span>
<span data-ttu-id="4ae1b-116">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="4ae1b-117">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="4ae1b-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="4ae1b-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ae1b-118">-Location</span></span>
<span data-ttu-id="4ae1b-119">Określa lokalizację, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="4ae1b-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4ae1b-120">Valid values are:</span></span> 
- <span data-ttu-id="4ae1b-121">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="4ae1b-121">North Central US</span></span>
- <span data-ttu-id="4ae1b-122">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="4ae1b-122">South Central US</span></span>
- <span data-ttu-id="4ae1b-123">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="4ae1b-123">Central US</span></span>
- <span data-ttu-id="4ae1b-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="4ae1b-124">West Europe</span></span>
- <span data-ttu-id="4ae1b-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="4ae1b-125">North Europe</span></span>
- <span data-ttu-id="4ae1b-126">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="4ae1b-126">West US</span></span>
- <span data-ttu-id="4ae1b-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="4ae1b-127">East US</span></span>
- <span data-ttu-id="4ae1b-128">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="4ae1b-128">East US 2</span></span>
- <span data-ttu-id="4ae1b-129">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="4ae1b-129">Japan East</span></span>
- <span data-ttu-id="4ae1b-130">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="4ae1b-130">Japan West</span></span>
- <span data-ttu-id="4ae1b-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="4ae1b-131">Brazil South</span></span>
- <span data-ttu-id="4ae1b-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="4ae1b-132">Southeast Asia</span></span>
- <span data-ttu-id="4ae1b-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="4ae1b-133">East Asia</span></span>
- <span data-ttu-id="4ae1b-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="4ae1b-134">Australia East</span></span>
- <span data-ttu-id="4ae1b-135">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="4ae1b-135">Australia Southeast</span></span>

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

### <span data-ttu-id="4ae1b-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4ae1b-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="4ae1b-137">Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="4ae1b-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ae1b-138">-Name</span></span>
<span data-ttu-id="4ae1b-139">Określa nazwę pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="4ae1b-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ae1b-140">-RedisConfiguration</span></span>
<span data-ttu-id="4ae1b-141">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="4ae1b-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4ae1b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ae1b-143">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="4ae1b-144">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="4ae1b-145">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-145">Premium tier only.</span></span>
- <span data-ttu-id="4ae1b-146">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="4ae1b-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="4ae1b-147">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="4ae1b-148">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-148">Premium tier only.</span></span>
- <span data-ttu-id="4ae1b-149">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="4ae1b-150">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="4ae1b-151">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-151">Premium tier only.</span></span> 
- <span data-ttu-id="4ae1b-152">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-152">maxmemory-reserved.</span></span>
<span data-ttu-id="4ae1b-153">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="4ae1b-154">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-155">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-155">maxmemory-policy.</span></span>
<span data-ttu-id="4ae1b-156">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="4ae1b-157">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-157">All pricing tiers.</span></span> 
- <span data-ttu-id="4ae1b-158">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-158">notify-keyspace-events.</span></span>
<span data-ttu-id="4ae1b-159">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="4ae1b-160">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-161">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="4ae1b-162">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4ae1b-163">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-164">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="4ae1b-165">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4ae1b-166">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-167">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-167">set-max-intset-entries.</span></span>
<span data-ttu-id="4ae1b-168">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4ae1b-169">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-170">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="4ae1b-171">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4ae1b-172">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-173">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="4ae1b-174">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4ae1b-175">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4ae1b-176">baz danych.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-176">databases.</span></span>
<span data-ttu-id="4ae1b-177">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-177">Configures the number of databases.</span></span>
<span data-ttu-id="4ae1b-178">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="4ae1b-179">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="4ae1b-180">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="4ae1b-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="4ae1b-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae1b-181">-ResourceGroupName</span></span>
<span data-ttu-id="4ae1b-182">Określa nazwę grupy zasobów, w której ma zostać utworzona pamięć podręczna Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="4ae1b-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="4ae1b-183">-ShardCount</span></span>
<span data-ttu-id="4ae1b-184">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="4ae1b-185">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4ae1b-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ae1b-186">jedno</span><span class="sxs-lookup"><span data-stu-id="4ae1b-186">1</span></span>
- <span data-ttu-id="4ae1b-187">2,6</span><span class="sxs-lookup"><span data-stu-id="4ae1b-187">2</span></span>
- <span data-ttu-id="4ae1b-188">3,2</span><span class="sxs-lookup"><span data-stu-id="4ae1b-188">3</span></span>
- <span data-ttu-id="4ae1b-189">r.[4</span><span class="sxs-lookup"><span data-stu-id="4ae1b-189">4</span></span>
- <span data-ttu-id="4ae1b-190">art</span><span class="sxs-lookup"><span data-stu-id="4ae1b-190">5</span></span>
- <span data-ttu-id="4ae1b-191">2,6</span><span class="sxs-lookup"><span data-stu-id="4ae1b-191">6</span></span>
- <span data-ttu-id="4ae1b-192">7,3</span><span class="sxs-lookup"><span data-stu-id="4ae1b-192">7</span></span>
- <span data-ttu-id="4ae1b-193">8</span><span class="sxs-lookup"><span data-stu-id="4ae1b-193">8</span></span>
- <span data-ttu-id="4ae1b-194">9</span><span class="sxs-lookup"><span data-stu-id="4ae1b-194">9</span></span> 
- <span data-ttu-id="4ae1b-195">dziesięciu</span><span class="sxs-lookup"><span data-stu-id="4ae1b-195">10</span></span>

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

### <span data-ttu-id="4ae1b-196">-Size</span><span class="sxs-lookup"><span data-stu-id="4ae1b-196">-Size</span></span>
<span data-ttu-id="4ae1b-197">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="4ae1b-198">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4ae1b-198">Valid values are:</span></span> 
- <span data-ttu-id="4ae1b-199">Punkt</span><span class="sxs-lookup"><span data-stu-id="4ae1b-199">P1</span></span>
- <span data-ttu-id="4ae1b-200">Punktu</span><span class="sxs-lookup"><span data-stu-id="4ae1b-200">P2</span></span>
- <span data-ttu-id="4ae1b-201">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="4ae1b-201">P3</span></span>
- <span data-ttu-id="4ae1b-202">P4</span><span class="sxs-lookup"><span data-stu-id="4ae1b-202">P4</span></span>
- <span data-ttu-id="4ae1b-203">P5</span><span class="sxs-lookup"><span data-stu-id="4ae1b-203">P5</span></span>
- <span data-ttu-id="4ae1b-204">C0</span><span class="sxs-lookup"><span data-stu-id="4ae1b-204">C0</span></span>
- <span data-ttu-id="4ae1b-205">C1</span><span class="sxs-lookup"><span data-stu-id="4ae1b-205">C1</span></span>
- <span data-ttu-id="4ae1b-206">C2</span><span class="sxs-lookup"><span data-stu-id="4ae1b-206">C2</span></span>
- <span data-ttu-id="4ae1b-207">C3</span><span class="sxs-lookup"><span data-stu-id="4ae1b-207">C3</span></span>
- <span data-ttu-id="4ae1b-208">C4</span><span class="sxs-lookup"><span data-stu-id="4ae1b-208">C4</span></span>
- <span data-ttu-id="4ae1b-209">C5</span><span class="sxs-lookup"><span data-stu-id="4ae1b-209">C5</span></span>
- <span data-ttu-id="4ae1b-210">C6</span><span class="sxs-lookup"><span data-stu-id="4ae1b-210">C6</span></span>
- <span data-ttu-id="4ae1b-211">250MB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-211">250MB</span></span>
- <span data-ttu-id="4ae1b-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-212">1GB</span></span>
- <span data-ttu-id="4ae1b-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-213">2.5GB</span></span>
- <span data-ttu-id="4ae1b-214">6GB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-214">6GB</span></span>
- <span data-ttu-id="4ae1b-215">13GB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-215">13GB</span></span>
- <span data-ttu-id="4ae1b-216">26GB</span><span class="sxs-lookup"><span data-stu-id="4ae1b-216">26GB</span></span>
- <span data-ttu-id="4ae1b-217">53GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="4ae1b-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="4ae1b-218">-Sku</span></span>
<span data-ttu-id="4ae1b-219">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="4ae1b-220">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4ae1b-220">Valid values are:</span></span> 
- <span data-ttu-id="4ae1b-221">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="4ae1b-221">Basic</span></span>
- <span data-ttu-id="4ae1b-222">Standard</span><span class="sxs-lookup"><span data-stu-id="4ae1b-222">Standard</span></span>
- <span data-ttu-id="4ae1b-223">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="4ae1b-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="4ae1b-224">-StaticIP</span></span>
<span data-ttu-id="4ae1b-225">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="4ae1b-226">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="4ae1b-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4ae1b-227">-SubnetId</span></span>
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

### <span data-ttu-id="4ae1b-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ae1b-228">-Tag</span></span>
<span data-ttu-id="4ae1b-229">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="4ae1b-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="4ae1b-230">-TenantSettings</span></span>
<span data-ttu-id="4ae1b-231">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="4ae1b-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="4ae1b-232">-Zone</span></span>
<span data-ttu-id="4ae1b-233">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-233">List of zones.</span></span>

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

### <span data-ttu-id="4ae1b-234">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ae1b-234">-Confirm</span></span>
<span data-ttu-id="4ae1b-235">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae1b-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae1b-236">-WhatIf</span></span>
<span data-ttu-id="4ae1b-237">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ae1b-238">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae1b-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae1b-239">CommonParameters</span></span>
<span data-ttu-id="4ae1b-240">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae1b-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae1b-241">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ae1b-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae1b-242">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ae1b-242">INPUTS</span></span>

### <span data-ttu-id="4ae1b-243">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae1b-243">System.String</span></span>

### <span data-ttu-id="4ae1b-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ae1b-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4ae1b-245">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ae1b-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ae1b-246">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ae1b-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ae1b-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="4ae1b-247">System.String[]</span></span>

## <span data-ttu-id="4ae1b-248">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ae1b-248">OUTPUTS</span></span>

### <span data-ttu-id="4ae1b-249">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4ae1b-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="4ae1b-250">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ae1b-250">NOTES</span></span>

## <span data-ttu-id="4ae1b-251">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ae1b-251">RELATED LINKS</span></span>

[<span data-ttu-id="4ae1b-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ae1b-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4ae1b-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ae1b-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4ae1b-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ae1b-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


