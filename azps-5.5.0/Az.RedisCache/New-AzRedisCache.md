---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183795"
---
# <span data-ttu-id="a8a0a-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8a0a-101">New-AzRedisCache</span></span>

## <span data-ttu-id="a8a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a0a-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="a8a0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8a0a-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8a0a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a0a-106">Polecenie **cmdlet New-AzRedisCache** tworzy pamięć podręczną Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="a8a0a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8a0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a0a-108">Przykład 1. Tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="a8a0a-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="a8a0a-109">To polecenie tworzy pamięć podręczną redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="a8a0a-110">Przykład 2. Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="a8a0a-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="a8a0a-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="a8a0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8a0a-112">PARAMETERS</span></span>

### <span data-ttu-id="a8a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="a8a0a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8a0a-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="a8a0a-115">-EnableNonSslPort</span></span>
<span data-ttu-id="a8a0a-116">Wskazuje, czy port bez protokołu SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="a8a0a-117">Wartość domyślna to $False (port niebędący protokołem SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="a8a0a-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="a8a0a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a8a0a-118">-Location</span></span>
<span data-ttu-id="a8a0a-119">Określa lokalizację, w której ma być tworzyć pamięć podręczną redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="a8a0a-120">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="a8a0a-120">Valid values are:</span></span> 
- <span data-ttu-id="a8a0a-121">North Central US</span><span class="sxs-lookup"><span data-stu-id="a8a0a-121">North Central US</span></span>
- <span data-ttu-id="a8a0a-122">South Central US</span><span class="sxs-lookup"><span data-stu-id="a8a0a-122">South Central US</span></span>
- <span data-ttu-id="a8a0a-123">Środkowe Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="a8a0a-123">Central US</span></span>
- <span data-ttu-id="a8a0a-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="a8a0a-124">West Europe</span></span>
- <span data-ttu-id="a8a0a-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="a8a0a-125">North Europe</span></span>
- <span data-ttu-id="a8a0a-126">Stany Zjednoczone Zachód</span><span class="sxs-lookup"><span data-stu-id="a8a0a-126">West US</span></span>
- <span data-ttu-id="a8a0a-127">Wschód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="a8a0a-127">East US</span></span>
- <span data-ttu-id="a8a0a-128">Wschód STANÓW ZJEDNOCZONYCH 2</span><span class="sxs-lookup"><span data-stu-id="a8a0a-128">East US 2</span></span>
- <span data-ttu-id="a8a0a-129">Japonia (Wschód)</span><span class="sxs-lookup"><span data-stu-id="a8a0a-129">Japan East</span></span>
- <span data-ttu-id="a8a0a-130">Japonia Zachód</span><span class="sxs-lookup"><span data-stu-id="a8a0a-130">Japan West</span></span>
- <span data-ttu-id="a8a0a-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="a8a0a-131">Brazil South</span></span>
- <span data-ttu-id="a8a0a-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="a8a0a-132">Southeast Asia</span></span>
- <span data-ttu-id="a8a0a-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="a8a0a-133">East Asia</span></span>
- <span data-ttu-id="a8a0a-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="a8a0a-134">Australia East</span></span>
- <span data-ttu-id="a8a0a-135">Australia Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="a8a0a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="a8a0a-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a8a0a-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="a8a0a-137">Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="a8a0a-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8a0a-138">-Name</span></span>
<span data-ttu-id="a8a0a-139">Określa nazwę pamięci podręcznej Redis, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="a8a0a-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8a0a-140">-RedisConfiguration</span></span>
<span data-ttu-id="a8a0a-141">Określa ustawienia konfiguracji programu Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="a8a0a-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a8a0a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8a0a-143">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="a8a0a-144">Określa, czy jest włączona funkcja zachowywania danych Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="a8a0a-145">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-145">Premium tier only.</span></span>
- <span data-ttu-id="a8a0a-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="a8a0a-147">Określa ciąg połączenia z kontem magazynu w celu ponownego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="a8a0a-148">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-148">Premium tier only.</span></span>
- <span data-ttu-id="a8a0a-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="a8a0a-150">Określa częstotliwość tworzenia kopii zapasowej dla zachowywania danych redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="a8a0a-151">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-151">Premium tier only.</span></span> 
- <span data-ttu-id="a8a0a-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-152">maxmemory-reserved.</span></span>
<span data-ttu-id="a8a0a-153">Konfiguruje pamięć zarezerwowaną dla procesów niebędące pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="a8a0a-154">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-155">maxmemory-policy.</span></span>
<span data-ttu-id="a8a0a-156">Konfiguruje zasady eksmisji dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="a8a0a-157">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-157">All pricing tiers.</span></span> 
- <span data-ttu-id="a8a0a-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-158">notify-keyspace-events.</span></span>
<span data-ttu-id="a8a0a-159">Konfiguruje powiadomienia keyspace.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="a8a0a-160">Warstwy standardowe i premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="a8a0a-162">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a8a0a-163">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="a8a0a-165">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a8a0a-166">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-167">set-max-intset-entries.</span></span>
<span data-ttu-id="a8a0a-168">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a8a0a-169">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="a8a0a-171">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a8a0a-172">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="a8a0a-174">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a8a0a-175">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a8a0a-176">baz danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-176">databases.</span></span>
<span data-ttu-id="a8a0a-177">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-177">Configures the number of databases.</span></span>
<span data-ttu-id="a8a0a-178">Tę właściwość można skonfigurować tylko podczas tworzenia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="a8a0a-179">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="a8a0a-180">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) (.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="a8a0a-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a0a-181">-ResourceGroupName</span></span>
<span data-ttu-id="a8a0a-182">Określa nazwę grupy zasobów, w której ma być tworzyć pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="a8a0a-183">-S scount</span><span class="sxs-lookup"><span data-stu-id="a8a0a-183">-ShardCount</span></span>
<span data-ttu-id="a8a0a-184">Określa liczbę plików do utworzenia w pamięci podręcznej klastrów Premium.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="a8a0a-185">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a8a0a-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8a0a-186">1</span><span class="sxs-lookup"><span data-stu-id="a8a0a-186">1</span></span>
- <span data-ttu-id="a8a0a-187">2</span><span class="sxs-lookup"><span data-stu-id="a8a0a-187">2</span></span>
- <span data-ttu-id="a8a0a-188">3</span><span class="sxs-lookup"><span data-stu-id="a8a0a-188">3</span></span>
- <span data-ttu-id="a8a0a-189">4</span><span class="sxs-lookup"><span data-stu-id="a8a0a-189">4</span></span>
- <span data-ttu-id="a8a0a-190">5</span><span class="sxs-lookup"><span data-stu-id="a8a0a-190">5</span></span>
- <span data-ttu-id="a8a0a-191">6</span><span class="sxs-lookup"><span data-stu-id="a8a0a-191">6</span></span>
- <span data-ttu-id="a8a0a-192">7</span><span class="sxs-lookup"><span data-stu-id="a8a0a-192">7</span></span>
- <span data-ttu-id="a8a0a-193">8</span><span class="sxs-lookup"><span data-stu-id="a8a0a-193">8</span></span>
- <span data-ttu-id="a8a0a-194">9</span><span class="sxs-lookup"><span data-stu-id="a8a0a-194">9</span></span> 
- <span data-ttu-id="a8a0a-195">10</span><span class="sxs-lookup"><span data-stu-id="a8a0a-195">10</span></span>

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

### <span data-ttu-id="a8a0a-196">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="a8a0a-196">-Size</span></span>
<span data-ttu-id="a8a0a-197">Określa rozmiar pamięci podręcznej Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="a8a0a-198">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="a8a0a-198">Valid values are:</span></span> 
- <span data-ttu-id="a8a0a-199">P1</span><span class="sxs-lookup"><span data-stu-id="a8a0a-199">P1</span></span>
- <span data-ttu-id="a8a0a-200">P2</span><span class="sxs-lookup"><span data-stu-id="a8a0a-200">P2</span></span>
- <span data-ttu-id="a8a0a-201">P3</span><span class="sxs-lookup"><span data-stu-id="a8a0a-201">P3</span></span>
- <span data-ttu-id="a8a0a-202">P4</span><span class="sxs-lookup"><span data-stu-id="a8a0a-202">P4</span></span>
- <span data-ttu-id="a8a0a-203">P5</span><span class="sxs-lookup"><span data-stu-id="a8a0a-203">P5</span></span>
- <span data-ttu-id="a8a0a-204">C0</span><span class="sxs-lookup"><span data-stu-id="a8a0a-204">C0</span></span>
- <span data-ttu-id="a8a0a-205">C1</span><span class="sxs-lookup"><span data-stu-id="a8a0a-205">C1</span></span>
- <span data-ttu-id="a8a0a-206">C2</span><span class="sxs-lookup"><span data-stu-id="a8a0a-206">C2</span></span>
- <span data-ttu-id="a8a0a-207">C3</span><span class="sxs-lookup"><span data-stu-id="a8a0a-207">C3</span></span>
- <span data-ttu-id="a8a0a-208">C4</span><span class="sxs-lookup"><span data-stu-id="a8a0a-208">C4</span></span>
- <span data-ttu-id="a8a0a-209">C5</span><span class="sxs-lookup"><span data-stu-id="a8a0a-209">C5</span></span>
- <span data-ttu-id="a8a0a-210">C6</span><span class="sxs-lookup"><span data-stu-id="a8a0a-210">C6</span></span>
- <span data-ttu-id="a8a0a-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-211">250MB</span></span>
- <span data-ttu-id="a8a0a-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-212">1GB</span></span>
- <span data-ttu-id="a8a0a-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-213">2.5GB</span></span>
- <span data-ttu-id="a8a0a-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-214">6GB</span></span>
- <span data-ttu-id="a8a0a-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-215">13GB</span></span>
- <span data-ttu-id="a8a0a-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="a8a0a-216">26GB</span></span>
- <span data-ttu-id="a8a0a-217">53 GB Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="a8a0a-218">- SKU</span><span class="sxs-lookup"><span data-stu-id="a8a0a-218">-Sku</span></span>
<span data-ttu-id="a8a0a-219">Określa liczbę SKU pamięci podręcznej Redis, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="a8a0a-220">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="a8a0a-220">Valid values are:</span></span> 
- <span data-ttu-id="a8a0a-221">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="a8a0a-221">Basic</span></span>
- <span data-ttu-id="a8a0a-222">Standardowe</span><span class="sxs-lookup"><span data-stu-id="a8a0a-222">Standard</span></span>
- <span data-ttu-id="a8a0a-223">Premium Wartość domyślna to Standardowy.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="a8a0a-224">— Statyczny adresIP</span><span class="sxs-lookup"><span data-stu-id="a8a0a-224">-StaticIP</span></span>
<span data-ttu-id="a8a0a-225">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="a8a0a-226">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="a8a0a-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a8a0a-227">-SubnetId</span></span>
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

### <span data-ttu-id="a8a0a-228">— Tag</span><span class="sxs-lookup"><span data-stu-id="a8a0a-228">-Tag</span></span>
<span data-ttu-id="a8a0a-229">Tabela skrótów reprezentująca tagi.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="a8a0a-230">- TenantSettings</span><span class="sxs-lookup"><span data-stu-id="a8a0a-230">-TenantSettings</span></span>
<span data-ttu-id="a8a0a-231">Ten parametr został wycofany.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="a8a0a-232">— Strefa</span><span class="sxs-lookup"><span data-stu-id="a8a0a-232">-Zone</span></span>
<span data-ttu-id="a8a0a-233">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-233">List of zones.</span></span>

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

### <span data-ttu-id="a8a0a-234">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8a0a-234">-Confirm</span></span>
<span data-ttu-id="a8a0a-235">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a0a-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a0a-236">-WhatIf</span></span>
<span data-ttu-id="a8a0a-237">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8a0a-238">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a0a-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a0a-239">CommonParameters</span></span>
<span data-ttu-id="a8a0a-240">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a0a-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a0a-241">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8a0a-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a0a-242">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8a0a-242">INPUTS</span></span>

### <span data-ttu-id="a8a0a-243">System.String</span><span class="sxs-lookup"><span data-stu-id="a8a0a-243">System.String</span></span>

### <span data-ttu-id="a8a0a-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8a0a-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a8a0a-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8a0a-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a8a0a-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8a0a-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a8a0a-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a8a0a-247">System.String[]</span></span>

## <span data-ttu-id="a8a0a-248">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8a0a-248">OUTPUTS</span></span>

### <span data-ttu-id="a8a0a-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a8a0a-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="a8a0a-250">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8a0a-250">NOTES</span></span>

## <span data-ttu-id="a8a0a-251">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8a0a-251">RELATED LINKS</span></span>

[<span data-ttu-id="a8a0a-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8a0a-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="a8a0a-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8a0a-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a8a0a-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8a0a-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


