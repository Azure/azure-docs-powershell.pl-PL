---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552576"
---
# <span data-ttu-id="f6410-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f6410-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="f6410-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6410-102">SYNOPSIS</span></span>
<span data-ttu-id="f6410-103">Modyfikuje pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="f6410-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6410-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6410-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6410-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6410-105">DESCRIPTION</span></span>
<span data-ttu-id="f6410-106">Polecenie cmdlet **Set-AzureRmRedisCache** modyfikuje pamięć podręczną platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="f6410-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="f6410-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6410-107">EXAMPLES</span></span>

### <span data-ttu-id="f6410-108">Przykład 1: modyfikowanie pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="f6410-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="f6410-109">To polecenie aktualizuje zasady maxmemory dla pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="f6410-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="f6410-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6410-110">PARAMETERS</span></span>

### <span data-ttu-id="f6410-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6410-111">-DefaultProfile</span></span>
<span data-ttu-id="f6410-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6410-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6410-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f6410-113">-EnableNonSslPort</span></span>
<span data-ttu-id="f6410-114">Wskazuje, czy port inny niż SSL jest włączony.</span><span class="sxs-lookup"><span data-stu-id="f6410-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f6410-115">Wartość domyślna to $False (port inny niż SSL jest wyłączony).</span><span class="sxs-lookup"><span data-stu-id="f6410-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f6410-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6410-116">-Name</span></span>
<span data-ttu-id="f6410-117">Określa nazwę pamięci podręcznej Redis do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f6410-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="f6410-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6410-118">-RedisConfiguration</span></span>
<span data-ttu-id="f6410-119">Określa ustawienia konfiguracji Redis.</span><span class="sxs-lookup"><span data-stu-id="f6410-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f6410-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6410-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6410-121">RDB — włączono funkcję kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f6410-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="f6410-122">Określa, że Redis danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f6410-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f6410-123">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-123">Premium tier only.</span></span>
- <span data-ttu-id="f6410-124">RDB-połączenie typu "pamięć podłączana".</span><span class="sxs-lookup"><span data-stu-id="f6410-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f6410-125">Określa parametry połączenia z kontem magazynu dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="f6410-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f6410-126">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-126">Premium tier only.</span></span>
- <span data-ttu-id="f6410-127">RDB — częstotliwość wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f6410-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="f6410-128">Określa częstotliwość wykonywania kopii zapasowych dla Redis danych.</span><span class="sxs-lookup"><span data-stu-id="f6410-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f6410-129">Tylko poziom Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-129">Premium tier only.</span></span> 
- <span data-ttu-id="f6410-130">maxmemory-zarezerwowane.</span><span class="sxs-lookup"><span data-stu-id="f6410-130">maxmemory-reserved.</span></span>
<span data-ttu-id="f6410-131">Konfiguruje pamięć zarezerwowaną dla procesów nieobsługujących pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f6410-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f6410-132">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-133">maxmemory — zasady.</span><span class="sxs-lookup"><span data-stu-id="f6410-133">maxmemory-policy.</span></span>
<span data-ttu-id="f6410-134">Konfiguruje zasady wykluczania dla pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f6410-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f6410-135">Wszystkie warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="f6410-135">All pricing tiers.</span></span> 
- <span data-ttu-id="f6410-136">Powiadamianie — zdarzenia dotyczące miejsca na znakach.</span><span class="sxs-lookup"><span data-stu-id="f6410-136">notify-keyspace-events.</span></span>
<span data-ttu-id="f6410-137">Konfiguruje powiadomienia dotyczące miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="f6410-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="f6410-138">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f6410-139">Hash-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="f6410-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f6410-140">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="f6410-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f6410-141">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-142">Hash — Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="f6410-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f6410-143">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="f6410-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f6410-144">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-145">set-max-intset-zapisy.</span><span class="sxs-lookup"><span data-stu-id="f6410-145">set-max-intset-entries.</span></span>
<span data-ttu-id="f6410-146">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="f6410-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f6410-147">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-148">zset-Max-ZipList-zapisy.</span><span class="sxs-lookup"><span data-stu-id="f6410-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f6410-149">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="f6410-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f6410-150">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-151">zset-Max-ZipList-Value.</span><span class="sxs-lookup"><span data-stu-id="f6410-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f6410-152">Konfiguruje optymalizację pamięci dla małych typów danych agregacji.</span><span class="sxs-lookup"><span data-stu-id="f6410-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f6410-153">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f6410-154">baz danych.</span><span class="sxs-lookup"><span data-stu-id="f6410-154">databases.</span></span>
<span data-ttu-id="f6410-155">Konfiguruje liczbę baz danych.</span><span class="sxs-lookup"><span data-stu-id="f6410-155">Configures the number of databases.</span></span>
<span data-ttu-id="f6410-156">Tę właściwość można skonfigurować tylko przy tworzeniu pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f6410-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f6410-157">Warstwy standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="f6410-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="f6410-158">Aby uzyskać więcej informacji, zobacz Zarządzanie usługą Azure Redis Cache za pomocą programu Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f6410-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f6410-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6410-159">-ResourceGroupName</span></span>
<span data-ttu-id="f6410-160">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="f6410-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="f6410-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f6410-161">-ShardCount</span></span>
<span data-ttu-id="f6410-162">Określa liczbę Shards, które mają być tworzone na Premium pamięci podręcznej klastra.</span><span class="sxs-lookup"><span data-stu-id="f6410-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="f6410-163">-Size</span><span class="sxs-lookup"><span data-stu-id="f6410-163">-Size</span></span>
<span data-ttu-id="f6410-164">Określa rozmiar pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="f6410-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f6410-165">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f6410-165">Valid values are:</span></span> 
- <span data-ttu-id="f6410-166">Punkt</span><span class="sxs-lookup"><span data-stu-id="f6410-166">P1</span></span>
- <span data-ttu-id="f6410-167">Punktu</span><span class="sxs-lookup"><span data-stu-id="f6410-167">P2</span></span>
- <span data-ttu-id="f6410-168">Przeznaczone</span><span class="sxs-lookup"><span data-stu-id="f6410-168">P3</span></span>
- <span data-ttu-id="f6410-169">P4</span><span class="sxs-lookup"><span data-stu-id="f6410-169">P4</span></span>
- <span data-ttu-id="f6410-170">C0</span><span class="sxs-lookup"><span data-stu-id="f6410-170">C0</span></span>
- <span data-ttu-id="f6410-171">C1</span><span class="sxs-lookup"><span data-stu-id="f6410-171">C1</span></span>
- <span data-ttu-id="f6410-172">C2</span><span class="sxs-lookup"><span data-stu-id="f6410-172">C2</span></span>
- <span data-ttu-id="f6410-173">C3</span><span class="sxs-lookup"><span data-stu-id="f6410-173">C3</span></span>
- <span data-ttu-id="f6410-174">C4</span><span class="sxs-lookup"><span data-stu-id="f6410-174">C4</span></span>
- <span data-ttu-id="f6410-175">C5</span><span class="sxs-lookup"><span data-stu-id="f6410-175">C5</span></span>
- <span data-ttu-id="f6410-176">C6</span><span class="sxs-lookup"><span data-stu-id="f6410-176">C6</span></span>
- <span data-ttu-id="f6410-177">250MB</span><span class="sxs-lookup"><span data-stu-id="f6410-177">250MB</span></span>
- <span data-ttu-id="f6410-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="f6410-178">1GB</span></span>
- <span data-ttu-id="f6410-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f6410-179">2.5GB</span></span>
- <span data-ttu-id="f6410-180">6GB</span><span class="sxs-lookup"><span data-stu-id="f6410-180">6GB</span></span>
- <span data-ttu-id="f6410-181">13GB</span><span class="sxs-lookup"><span data-stu-id="f6410-181">13GB</span></span>
- <span data-ttu-id="f6410-182">26GB</span><span class="sxs-lookup"><span data-stu-id="f6410-182">26GB</span></span>
- <span data-ttu-id="f6410-183">53GB wartość domyślna to 1 GB lub C1.</span><span class="sxs-lookup"><span data-stu-id="f6410-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f6410-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6410-184">-Sku</span></span>
<span data-ttu-id="f6410-185">Określa jednostkę SKU pamięci podręcznej Redis do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f6410-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f6410-186">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f6410-186">Valid values are:</span></span> 
- <span data-ttu-id="f6410-187">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="f6410-187">Basic</span></span>
- <span data-ttu-id="f6410-188">Standard</span><span class="sxs-lookup"><span data-stu-id="f6410-188">Standard</span></span>
- <span data-ttu-id="f6410-189">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="f6410-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="f6410-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6410-190">-Tag</span></span>
<span data-ttu-id="f6410-191">Tabela skrótów przedstawiająca znaczniki.</span><span class="sxs-lookup"><span data-stu-id="f6410-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="f6410-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f6410-192">-TenantSettings</span></span>
<span data-ttu-id="f6410-193">Ten parametr jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="f6410-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f6410-194">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6410-194">-Confirm</span></span>
<span data-ttu-id="f6410-195">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6410-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6410-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6410-196">-WhatIf</span></span>
<span data-ttu-id="f6410-197">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6410-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6410-198">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6410-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6410-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6410-199">CommonParameters</span></span>
<span data-ttu-id="f6410-200">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6410-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6410-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6410-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6410-202">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6410-202">INPUTS</span></span>

### <span data-ttu-id="f6410-203">System. String</span><span class="sxs-lookup"><span data-stu-id="f6410-203">System.String</span></span>

### <span data-ttu-id="f6410-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6410-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f6410-205">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f6410-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f6410-206">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f6410-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f6410-207">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6410-207">OUTPUTS</span></span>

### <span data-ttu-id="f6410-208">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f6410-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f6410-209">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6410-209">NOTES</span></span>

## <span data-ttu-id="f6410-210">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6410-210">RELATED LINKS</span></span>

[<span data-ttu-id="f6410-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f6410-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="f6410-212">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f6410-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f6410-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f6410-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


