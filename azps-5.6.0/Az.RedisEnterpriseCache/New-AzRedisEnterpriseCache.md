---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: 43ad21450666fb2db9a25e1e2803651eacf511d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000762"
---
# <span data-ttu-id="7a233-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="7a233-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="7a233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a233-102">SYNOPSIS</span></span>
<span data-ttu-id="7a233-103">Tworzy klaster pamięci podręcznej Redis Enterpise i skojarzoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7a233-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="7a233-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a233-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a233-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a233-105">DESCRIPTION</span></span>
<span data-ttu-id="7a233-106">Tworzy lub aktualizuje istniejący (zastępowanie/ponowne, z potencjalnymi przestojami) klaster pamięci podręcznej i skojarzoną bazę danych o nazwie "domyślna"</span><span class="sxs-lookup"><span data-stu-id="7a233-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="7a233-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a233-107">EXAMPLES</span></span>

### <span data-ttu-id="7a233-108">Przykład 1. Tworzenie pamięci podręcznej Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="7a233-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="7a233-109">To polecenie tworzy pamięć podręczną Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="7a233-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="7a233-110">Przykład 2. Tworzenie pamięci podręcznej Redis Enterprise Cache przy użyciu niektórych parametrów opcjonalnych</span><span class="sxs-lookup"><span data-stu-id="7a233-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="7a233-111">To polecenie tworzy pamięć podręczną Redis Enterprise Cache o nazwie MyCache, używając niektórych parametrów opcjonalnych.</span><span class="sxs-lookup"><span data-stu-id="7a233-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="7a233-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a233-112">PARAMETERS</span></span>

### <span data-ttu-id="7a233-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7a233-113">-AsJob</span></span>
<span data-ttu-id="7a233-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7a233-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-115">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="7a233-115">-Capacity</span></span>
<span data-ttu-id="7a233-116">Rozmiar klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="7a233-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="7a233-117">Wartość domyślna to 2 lub 3 w zależności od typu SKU.</span><span class="sxs-lookup"><span data-stu-id="7a233-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="7a233-118">Prawidłowe wartości to (2, 4, 6, ...) dla wersji Enterprise i (3, 9, 15, ...) dla wersji Flash.</span><span class="sxs-lookup"><span data-stu-id="7a233-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7a233-119">-ClientProtocol</span></span>
<span data-ttu-id="7a233-120">Określa, czy klienci redis mogą łączyć się przy użyciu protokołów TLS-encrypted, czy zwykłego tekstu redis.</span><span class="sxs-lookup"><span data-stu-id="7a233-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="7a233-121">Wartością domyślną jest szyfrowanie TLS.</span><span class="sxs-lookup"><span data-stu-id="7a233-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-122">- ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="7a233-122">-ClusteringPolicy</span></span>
<span data-ttu-id="7a233-123">Zasady klastrowania — domyślne ustawienie to OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="7a233-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="7a233-124">Określony w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="7a233-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a233-125">-ClusterName</span></span>
<span data-ttu-id="7a233-126">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="7a233-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a233-127">-DefaultProfile</span></span>
<span data-ttu-id="7a233-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a233-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a233-129">-EvictionPolicy</span></span>
<span data-ttu-id="7a233-130">Zasady ponownego wywłasowania — wartością domyślną jest NietrwałaLRU.</span><span class="sxs-lookup"><span data-stu-id="7a233-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7a233-131">-Location</span></span>
<span data-ttu-id="7a233-132">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="7a233-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7a233-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="7a233-134">Minimalna wersja TLS dla klastra do obsługi, na przykład 1,2</span><span class="sxs-lookup"><span data-stu-id="7a233-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-135">— Moduł</span><span class="sxs-lookup"><span data-stu-id="7a233-135">-Module</span></span>
<span data-ttu-id="7a233-136">Opcjonalny zestaw modułów redis umożliwiających włączenie w tej bazie danych — moduły można dodawać tylko podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="7a233-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="7a233-137">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach modułu i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="7a233-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a233-138">-NoWait</span></span>
<span data-ttu-id="7a233-139">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7a233-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-140">— Port</span><span class="sxs-lookup"><span data-stu-id="7a233-140">-Port</span></span>
<span data-ttu-id="7a233-141">Port TCP punktu końcowego bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7a233-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="7a233-142">Określony w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="7a233-142">Specified at create time.</span></span>
<span data-ttu-id="7a233-143">Domyślnie jest to dostępny port.</span><span class="sxs-lookup"><span data-stu-id="7a233-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a233-144">-ResourceGroupName</span></span>
<span data-ttu-id="7a233-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a233-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-146">- SKU</span><span class="sxs-lookup"><span data-stu-id="7a233-146">-Sku</span></span>
<span data-ttu-id="7a233-147">Typ klastrów RedisEnterprise do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="7a233-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="7a233-148">Możliwe wartości: (Enterprise_E10, EnterpriseFlash_F300 itp.)</span><span class="sxs-lookup"><span data-stu-id="7a233-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-149">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a233-149">-SubscriptionId</span></span>
<span data-ttu-id="7a233-150">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a233-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7a233-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7a233-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-152">— Tag</span><span class="sxs-lookup"><span data-stu-id="7a233-152">-Tag</span></span>
<span data-ttu-id="7a233-153">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a233-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-154">— Strefa</span><span class="sxs-lookup"><span data-stu-id="7a233-154">-Zone</span></span>
<span data-ttu-id="7a233-155">Strefy, w których ten klaster zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="7a233-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a233-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a233-156">-Confirm</span></span>
<span data-ttu-id="7a233-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a233-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a233-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a233-158">-WhatIf</span></span>
<span data-ttu-id="7a233-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a233-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a233-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a233-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a233-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a233-161">CommonParameters</span></span>
<span data-ttu-id="7a233-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a233-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a233-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a233-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a233-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a233-164">INPUTS</span></span>

## <span data-ttu-id="7a233-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a233-165">OUTPUTS</span></span>

### <span data-ttu-id="7a233-166">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="7a233-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="7a233-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a233-167">NOTES</span></span>

<span data-ttu-id="7a233-168">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7a233-168">ALIASES</span></span>

<span data-ttu-id="7a233-169">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a233-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a233-170">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7a233-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a233-171">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a233-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a233-172">MODULE <IModule[]>: Opcjonalny zestaw modułów redis umożliwiających włączenie w tej bazie danych — moduły można dodawać tylko podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="7a233-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="7a233-173">`Name <String>`: nazwa modułu, na przykład "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="7a233-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="7a233-174">`[Arg <String>]`: Opcje konfiguracji modułu, na przykład "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="7a233-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="7a233-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a233-175">RELATED LINKS</span></span>

