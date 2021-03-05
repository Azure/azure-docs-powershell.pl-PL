---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000913"
---
# <span data-ttu-id="95d58-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="95d58-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="95d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d58-102">SYNOPSIS</span></span>
<span data-ttu-id="95d58-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="95d58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95d58-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d58-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="95d58-105">DESCRIPTION</span></span>
<span data-ttu-id="95d58-106">Polecenie **cmdlet Set-AzRedisCache modyfikuje** pamięć podręczną Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="95d58-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="95d58-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95d58-107">EXAMPLES</span></span>

### <span data-ttu-id="95d58-108">Przykład 1. Modyfikowanie pamięci podręcznej redis</span><span class="sxs-lookup"><span data-stu-id="95d58-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="95d58-109">To polecenie aktualizuje zasady maksmemory dla funkcji Redis Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="95d58-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="95d58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d58-110">PARAMETERS</span></span>

### <span data-ttu-id="95d58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d58-111">-DefaultProfile</span></span>
<span data-ttu-id="95d58-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95d58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d58-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="95d58-113">-EnableNonSslPort</span></span>
<span data-ttu-id="95d58-114">Wskazuje, czy port bez protokołu SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="95d58-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="95d58-115">Wartość domyślna to $False (port niebędący protokołem SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="95d58-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="95d58-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="95d58-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="95d58-117">Określ wersję TLS wymaganą przez klientów do łączenia się z pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="95d58-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="95d58-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="95d58-118">-Name</span></span>
<span data-ttu-id="95d58-119">Określa nazwę pamięci podręcznej Redis, która ma być aktualizowana.</span><span class="sxs-lookup"><span data-stu-id="95d58-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="95d58-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="95d58-120">-RedisConfiguration</span></span>
<span data-ttu-id="95d58-121">Określa ustawienia konfiguracji programu Redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="95d58-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="95d58-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95d58-123">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="95d58-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="95d58-124">Określa, czy jest włączona funkcja zachowywania danych Redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="95d58-125">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-125">Premium tier only.</span></span>
- <span data-ttu-id="95d58-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="95d58-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="95d58-127">Określa ciąg połączenia z kontem magazynu w celu ponownego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="95d58-128">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-128">Premium tier only.</span></span>
- <span data-ttu-id="95d58-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="95d58-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="95d58-130">Określa częstotliwość tworzenia kopii zapasowej dla zachowywania danych redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="95d58-131">Tylko warstwa premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-131">Premium tier only.</span></span> 
- <span data-ttu-id="95d58-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="95d58-132">maxmemory-reserved.</span></span>
<span data-ttu-id="95d58-133">Konfiguruje pamięć zarezerwowaną dla procesów niebędące pamięcią podręczną.</span><span class="sxs-lookup"><span data-stu-id="95d58-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="95d58-134">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="95d58-135">maxmemory-policy.</span></span>
<span data-ttu-id="95d58-136">Konfiguruje zasady eksmisji dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="95d58-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="95d58-137">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="95d58-137">All pricing tiers.</span></span> 
- <span data-ttu-id="95d58-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="95d58-138">notify-keyspace-events.</span></span>
<span data-ttu-id="95d58-139">Konfiguruje powiadomienia keyspace.</span><span class="sxs-lookup"><span data-stu-id="95d58-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="95d58-140">Warstwy standardowe i premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="95d58-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="95d58-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="95d58-142">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="95d58-143">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="95d58-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="95d58-145">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="95d58-146">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="95d58-147">set-max-intset-entries.</span></span>
<span data-ttu-id="95d58-148">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="95d58-149">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="95d58-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="95d58-151">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="95d58-152">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="95d58-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="95d58-154">Konfiguruje optymalizację pamięci dla małych, zagregowanych typów danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="95d58-155">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="95d58-156">baz danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-156">databases.</span></span>
<span data-ttu-id="95d58-157">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="95d58-157">Configures the number of databases.</span></span>
<span data-ttu-id="95d58-158">Tę właściwość można skonfigurować tylko podczas tworzenia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="95d58-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="95d58-159">Warstwy Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="95d58-160">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) (.</span><span class="sxs-lookup"><span data-stu-id="95d58-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="95d58-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d58-161">-ResourceGroupName</span></span>
<span data-ttu-id="95d58-162">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="95d58-163">-S scount</span><span class="sxs-lookup"><span data-stu-id="95d58-163">-ShardCount</span></span>
<span data-ttu-id="95d58-164">Określa liczbę plików do utworzenia w pamięci podręcznej klastrów Premium.</span><span class="sxs-lookup"><span data-stu-id="95d58-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="95d58-165">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="95d58-165">-Size</span></span>
<span data-ttu-id="95d58-166">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="95d58-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="95d58-167">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="95d58-167">Valid values are:</span></span> 
- <span data-ttu-id="95d58-168">P1</span><span class="sxs-lookup"><span data-stu-id="95d58-168">P1</span></span>
- <span data-ttu-id="95d58-169">P2</span><span class="sxs-lookup"><span data-stu-id="95d58-169">P2</span></span>
- <span data-ttu-id="95d58-170">P3</span><span class="sxs-lookup"><span data-stu-id="95d58-170">P3</span></span>
- <span data-ttu-id="95d58-171">P4</span><span class="sxs-lookup"><span data-stu-id="95d58-171">P4</span></span>
- <span data-ttu-id="95d58-172">P5</span><span class="sxs-lookup"><span data-stu-id="95d58-172">P5</span></span>
- <span data-ttu-id="95d58-173">C0</span><span class="sxs-lookup"><span data-stu-id="95d58-173">C0</span></span>
- <span data-ttu-id="95d58-174">C1</span><span class="sxs-lookup"><span data-stu-id="95d58-174">C1</span></span>
- <span data-ttu-id="95d58-175">C2</span><span class="sxs-lookup"><span data-stu-id="95d58-175">C2</span></span>
- <span data-ttu-id="95d58-176">C3</span><span class="sxs-lookup"><span data-stu-id="95d58-176">C3</span></span>
- <span data-ttu-id="95d58-177">C4</span><span class="sxs-lookup"><span data-stu-id="95d58-177">C4</span></span>
- <span data-ttu-id="95d58-178">C5</span><span class="sxs-lookup"><span data-stu-id="95d58-178">C5</span></span>
- <span data-ttu-id="95d58-179">C6</span><span class="sxs-lookup"><span data-stu-id="95d58-179">C6</span></span>
- <span data-ttu-id="95d58-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="95d58-180">250MB</span></span>
- <span data-ttu-id="95d58-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-181">1GB</span></span>
- <span data-ttu-id="95d58-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-182">2.5GB</span></span>
- <span data-ttu-id="95d58-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-183">6GB</span></span>
- <span data-ttu-id="95d58-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-184">13GB</span></span>
- <span data-ttu-id="95d58-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-185">26GB</span></span>
- <span data-ttu-id="95d58-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="95d58-186">53GB</span></span>
- <span data-ttu-id="95d58-187">120 GB Wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="95d58-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="95d58-188">- SKU</span><span class="sxs-lookup"><span data-stu-id="95d58-188">-Sku</span></span>
<span data-ttu-id="95d58-189">Określa liczbę SKU pamięci podręcznej Redis, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="95d58-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="95d58-190">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="95d58-190">Valid values are:</span></span> 
- <span data-ttu-id="95d58-191">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="95d58-191">Basic</span></span>
- <span data-ttu-id="95d58-192">Standardowe</span><span class="sxs-lookup"><span data-stu-id="95d58-192">Standard</span></span>
- <span data-ttu-id="95d58-193">Premium Wartość domyślna to Standardowy.</span><span class="sxs-lookup"><span data-stu-id="95d58-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="95d58-194">— Tag</span><span class="sxs-lookup"><span data-stu-id="95d58-194">-Tag</span></span>
<span data-ttu-id="95d58-195">Tabela skrótów reprezentująca tagi.</span><span class="sxs-lookup"><span data-stu-id="95d58-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="95d58-196">- TenantSettings</span><span class="sxs-lookup"><span data-stu-id="95d58-196">-TenantSettings</span></span>
<span data-ttu-id="95d58-197">Ten parametr został wycofany.</span><span class="sxs-lookup"><span data-stu-id="95d58-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="95d58-198">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95d58-198">-Confirm</span></span>
<span data-ttu-id="95d58-199">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95d58-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d58-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d58-200">-WhatIf</span></span>
<span data-ttu-id="95d58-201">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d58-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95d58-202">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95d58-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d58-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d58-203">CommonParameters</span></span>
<span data-ttu-id="95d58-204">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d58-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d58-205">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95d58-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d58-206">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95d58-206">INPUTS</span></span>

### <span data-ttu-id="95d58-207">System.String</span><span class="sxs-lookup"><span data-stu-id="95d58-207">System.String</span></span>

### <span data-ttu-id="95d58-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95d58-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95d58-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95d58-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="95d58-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95d58-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="95d58-211">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95d58-211">OUTPUTS</span></span>

### <span data-ttu-id="95d58-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="95d58-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="95d58-213">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95d58-213">NOTES</span></span>

## <span data-ttu-id="95d58-214">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95d58-214">RELATED LINKS</span></span>

[<span data-ttu-id="95d58-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="95d58-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="95d58-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="95d58-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="95d58-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="95d58-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


