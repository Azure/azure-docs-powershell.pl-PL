---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997368"
---
# <span data-ttu-id="d6df0-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6df0-101">New-AzRedisCache</span></span>

## <span data-ttu-id="d6df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6df0-102">SYNOPSIS</span></span>
<span data-ttu-id="d6df0-103">Tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="d6df0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6df0-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6df0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6df0-105">DESCRIPTION</span></span>
<span data-ttu-id="d6df0-106">Polecenie **cmdlet New-AzRedisCache** tworzy pamięć podręczną Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="d6df0-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d6df0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6df0-107">EXAMPLES</span></span>

### <span data-ttu-id="d6df0-108">Przykład 1. Tworzenie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="d6df0-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="d6df0-109">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d6df0-110">Przykład 2. Tworzenie standardowej pamięci podręcznej Redis SKU</span><span class="sxs-lookup"><span data-stu-id="d6df0-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="d6df0-111">To polecenie tworzy pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d6df0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6df0-112">PARAMETERS</span></span>

### <span data-ttu-id="d6df0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6df0-113">-DefaultProfile</span></span>
<span data-ttu-id="d6df0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6df0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6df0-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d6df0-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d6df0-116">Wskazuje, czy port bez protokołu SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="d6df0-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d6df0-117">Wartość domyślna to $False (port niebędący protokołem SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="d6df0-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d6df0-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d6df0-118">-Location</span></span>
<span data-ttu-id="d6df0-119">Określa lokalizację, w której ma być tworzyć pamięć podręczną redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d6df0-120">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="d6df0-120">Valid values are:</span></span> 
- <span data-ttu-id="d6df0-121">North Central US</span><span class="sxs-lookup"><span data-stu-id="d6df0-121">North Central US</span></span>
- <span data-ttu-id="d6df0-122">South Central US</span><span class="sxs-lookup"><span data-stu-id="d6df0-122">South Central US</span></span>
- <span data-ttu-id="d6df0-123">Środkowe Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="d6df0-123">Central US</span></span>
- <span data-ttu-id="d6df0-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="d6df0-124">West Europe</span></span>
- <span data-ttu-id="d6df0-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="d6df0-125">North Europe</span></span>
- <span data-ttu-id="d6df0-126">Stany Zjednoczone Zachód</span><span class="sxs-lookup"><span data-stu-id="d6df0-126">West US</span></span>
- <span data-ttu-id="d6df0-127">Wschód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="d6df0-127">East US</span></span>
- <span data-ttu-id="d6df0-128">Wschód STANÓW ZJEDNOCZONYCH 2</span><span class="sxs-lookup"><span data-stu-id="d6df0-128">East US 2</span></span>
- <span data-ttu-id="d6df0-129">Japonia (Wschód)</span><span class="sxs-lookup"><span data-stu-id="d6df0-129">Japan East</span></span>
- <span data-ttu-id="d6df0-130">Japonia Zachód</span><span class="sxs-lookup"><span data-stu-id="d6df0-130">Japan West</span></span>
- <span data-ttu-id="d6df0-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="d6df0-131">Brazil South</span></span>
- <span data-ttu-id="d6df0-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d6df0-132">Southeast Asia</span></span>
- <span data-ttu-id="d6df0-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d6df0-133">East Asia</span></span>
- <span data-ttu-id="d6df0-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d6df0-134">Australia East</span></span>
- <span data-ttu-id="d6df0-135">Australia Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="d6df0-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d6df0-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d6df0-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="d6df0-137">Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="d6df0-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="d6df0-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6df0-138">-Name</span></span>
<span data-ttu-id="d6df0-139">Określa nazwę pamięci podręcznej Redis, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="d6df0-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d6df0-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6df0-140">-RedisConfiguration</span></span>
<span data-ttu-id="d6df0-141">Określa ustawienia konfiguracji programu Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d6df0-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6df0-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6df0-143">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="d6df0-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="d6df0-144">Określa, czy jest włączona funkcja zachowywania danych Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d6df0-145">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-145">Premium tier only.</span></span>
- <span data-ttu-id="d6df0-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="d6df0-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d6df0-147">Określa ciąg połączenia z kontem magazynu w celu ponownego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d6df0-148">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-148">Premium tier only.</span></span>
- <span data-ttu-id="d6df0-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="d6df0-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="d6df0-150">Określa częstotliwość tworzenia kopii zapasowej dla zachowywania danych redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d6df0-151">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-151">Premium tier only.</span></span> 
- <span data-ttu-id="d6df0-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="d6df0-152">maxmemory-reserved.</span></span>
<span data-ttu-id="d6df0-153">Konfiguruje pamięć zarezerwowaną dla procesów niebędące pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="d6df0-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d6df0-154">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="d6df0-155">maxmemory-policy.</span></span>
<span data-ttu-id="d6df0-156">Konfiguruje zasady eksmisji dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d6df0-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d6df0-157">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="d6df0-157">All pricing tiers.</span></span> 
- <span data-ttu-id="d6df0-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="d6df0-158">notify-keyspace-events.</span></span>
<span data-ttu-id="d6df0-159">Konfiguruje powiadomienia keyspace.</span><span class="sxs-lookup"><span data-stu-id="d6df0-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="d6df0-160">Warstwy standardowe i premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d6df0-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="d6df0-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d6df0-162">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d6df0-163">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d6df0-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d6df0-165">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d6df0-166">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="d6df0-167">set-max-intset-entries.</span></span>
<span data-ttu-id="d6df0-168">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d6df0-169">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="d6df0-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d6df0-171">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d6df0-172">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d6df0-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d6df0-174">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d6df0-175">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d6df0-176">baz danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-176">databases.</span></span>
<span data-ttu-id="d6df0-177">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="d6df0-177">Configures the number of databases.</span></span>
<span data-ttu-id="d6df0-178">Tę właściwość można skonfigurować tylko podczas tworzenia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d6df0-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d6df0-179">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="d6df0-180">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) (.</span><span class="sxs-lookup"><span data-stu-id="d6df0-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d6df0-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6df0-181">-ResourceGroupName</span></span>
<span data-ttu-id="d6df0-182">Określa nazwę grupy zasobów, w której ma być tworzyć pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d6df0-183">-S scount</span><span class="sxs-lookup"><span data-stu-id="d6df0-183">-ShardCount</span></span>
<span data-ttu-id="d6df0-184">Określa liczbę plików do utworzenia w pamięci podręcznej klastrów Premium.</span><span class="sxs-lookup"><span data-stu-id="d6df0-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d6df0-185">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6df0-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6df0-186">1</span><span class="sxs-lookup"><span data-stu-id="d6df0-186">1</span></span>
- <span data-ttu-id="d6df0-187">2</span><span class="sxs-lookup"><span data-stu-id="d6df0-187">2</span></span>
- <span data-ttu-id="d6df0-188">3</span><span class="sxs-lookup"><span data-stu-id="d6df0-188">3</span></span>
- <span data-ttu-id="d6df0-189">4</span><span class="sxs-lookup"><span data-stu-id="d6df0-189">4</span></span>
- <span data-ttu-id="d6df0-190">5</span><span class="sxs-lookup"><span data-stu-id="d6df0-190">5</span></span>
- <span data-ttu-id="d6df0-191">6</span><span class="sxs-lookup"><span data-stu-id="d6df0-191">6</span></span>
- <span data-ttu-id="d6df0-192">7</span><span class="sxs-lookup"><span data-stu-id="d6df0-192">7</span></span>
- <span data-ttu-id="d6df0-193">8</span><span class="sxs-lookup"><span data-stu-id="d6df0-193">8</span></span>
- <span data-ttu-id="d6df0-194">9</span><span class="sxs-lookup"><span data-stu-id="d6df0-194">9</span></span> 
- <span data-ttu-id="d6df0-195">10</span><span class="sxs-lookup"><span data-stu-id="d6df0-195">10</span></span>

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

### <span data-ttu-id="d6df0-196">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="d6df0-196">-Size</span></span>
<span data-ttu-id="d6df0-197">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d6df0-198">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="d6df0-198">Valid values are:</span></span> 
- <span data-ttu-id="d6df0-199">P1</span><span class="sxs-lookup"><span data-stu-id="d6df0-199">P1</span></span>
- <span data-ttu-id="d6df0-200">P2</span><span class="sxs-lookup"><span data-stu-id="d6df0-200">P2</span></span>
- <span data-ttu-id="d6df0-201">P3</span><span class="sxs-lookup"><span data-stu-id="d6df0-201">P3</span></span>
- <span data-ttu-id="d6df0-202">P4</span><span class="sxs-lookup"><span data-stu-id="d6df0-202">P4</span></span>
- <span data-ttu-id="d6df0-203">P5</span><span class="sxs-lookup"><span data-stu-id="d6df0-203">P5</span></span>
- <span data-ttu-id="d6df0-204">C0</span><span class="sxs-lookup"><span data-stu-id="d6df0-204">C0</span></span>
- <span data-ttu-id="d6df0-205">C1</span><span class="sxs-lookup"><span data-stu-id="d6df0-205">C1</span></span>
- <span data-ttu-id="d6df0-206">C2</span><span class="sxs-lookup"><span data-stu-id="d6df0-206">C2</span></span>
- <span data-ttu-id="d6df0-207">C3</span><span class="sxs-lookup"><span data-stu-id="d6df0-207">C3</span></span>
- <span data-ttu-id="d6df0-208">C4</span><span class="sxs-lookup"><span data-stu-id="d6df0-208">C4</span></span>
- <span data-ttu-id="d6df0-209">C5</span><span class="sxs-lookup"><span data-stu-id="d6df0-209">C5</span></span>
- <span data-ttu-id="d6df0-210">C6</span><span class="sxs-lookup"><span data-stu-id="d6df0-210">C6</span></span>
- <span data-ttu-id="d6df0-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="d6df0-211">250MB</span></span>
- <span data-ttu-id="d6df0-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="d6df0-212">1GB</span></span>
- <span data-ttu-id="d6df0-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="d6df0-213">2.5GB</span></span>
- <span data-ttu-id="d6df0-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="d6df0-214">6GB</span></span>
- <span data-ttu-id="d6df0-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="d6df0-215">13GB</span></span>
- <span data-ttu-id="d6df0-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="d6df0-216">26GB</span></span>
- <span data-ttu-id="d6df0-217">53 GB Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="d6df0-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d6df0-218">- SKU</span><span class="sxs-lookup"><span data-stu-id="d6df0-218">-Sku</span></span>
<span data-ttu-id="d6df0-219">Określa liczbę SKU pamięci podręcznej Redis, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="d6df0-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d6df0-220">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="d6df0-220">Valid values are:</span></span> 
- <span data-ttu-id="d6df0-221">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="d6df0-221">Basic</span></span>
- <span data-ttu-id="d6df0-222">Standardowe</span><span class="sxs-lookup"><span data-stu-id="d6df0-222">Standard</span></span>
- <span data-ttu-id="d6df0-223">Premium Wartość domyślna to Standardowy.</span><span class="sxs-lookup"><span data-stu-id="d6df0-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="d6df0-224">— Statyczny adresIP</span><span class="sxs-lookup"><span data-stu-id="d6df0-224">-StaticIP</span></span>
<span data-ttu-id="d6df0-225">Określa unikatowy adres IP w podsieci dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d6df0-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="d6df0-226">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet wybierze adres IP z podsieci.</span><span class="sxs-lookup"><span data-stu-id="d6df0-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d6df0-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d6df0-227">-SubnetId</span></span>
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

### <span data-ttu-id="d6df0-228">— Tag</span><span class="sxs-lookup"><span data-stu-id="d6df0-228">-Tag</span></span>
<span data-ttu-id="d6df0-229">Tabela skrótów reprezentująca tagi.</span><span class="sxs-lookup"><span data-stu-id="d6df0-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d6df0-230">- TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d6df0-230">-TenantSettings</span></span>
<span data-ttu-id="d6df0-231">Ten parametr został wycofany.</span><span class="sxs-lookup"><span data-stu-id="d6df0-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d6df0-232">— Strefa</span><span class="sxs-lookup"><span data-stu-id="d6df0-232">-Zone</span></span>
<span data-ttu-id="d6df0-233">Lista stref.</span><span class="sxs-lookup"><span data-stu-id="d6df0-233">List of zones.</span></span>

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

### <span data-ttu-id="d6df0-234">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6df0-234">-Confirm</span></span>
<span data-ttu-id="d6df0-235">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6df0-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6df0-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6df0-236">-WhatIf</span></span>
<span data-ttu-id="d6df0-237">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6df0-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6df0-238">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6df0-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6df0-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6df0-239">CommonParameters</span></span>
<span data-ttu-id="d6df0-240">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6df0-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6df0-241">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6df0-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6df0-242">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6df0-242">INPUTS</span></span>

### <span data-ttu-id="d6df0-243">System.String</span><span class="sxs-lookup"><span data-stu-id="d6df0-243">System.String</span></span>

### <span data-ttu-id="d6df0-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6df0-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d6df0-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6df0-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6df0-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6df0-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6df0-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d6df0-247">System.String[]</span></span>

## <span data-ttu-id="d6df0-248">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6df0-248">OUTPUTS</span></span>

### <span data-ttu-id="d6df0-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d6df0-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="d6df0-250">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6df0-250">NOTES</span></span>

## <span data-ttu-id="d6df0-251">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6df0-251">RELATED LINKS</span></span>

[<span data-ttu-id="d6df0-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6df0-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d6df0-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6df0-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d6df0-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6df0-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


