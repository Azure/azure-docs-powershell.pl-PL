---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378226"
---
# <span data-ttu-id="660a1-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="660a1-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="660a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="660a1-102">SYNOPSIS</span></span>
<span data-ttu-id="660a1-103">Tworzy klaster pamięci podręcznej Redis enterpise i skojarzoną z nią bazę danych</span><span class="sxs-lookup"><span data-stu-id="660a1-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="660a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="660a1-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="660a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="660a1-105">DESCRIPTION</span></span>
<span data-ttu-id="660a1-106">Tworzy lub aktualizuje istniejące (zastępowanie/ponowne tworzenie) klaster pamięci podręcznej i skojarzoną z nią bazę danych o nazwie "default"</span><span class="sxs-lookup"><span data-stu-id="660a1-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="660a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="660a1-107">EXAMPLES</span></span>

### <span data-ttu-id="660a1-108">Przykład 1. Tworzenie Redis pamięci podręcznej przedsiębiorstwa</span><span class="sxs-lookup"><span data-stu-id="660a1-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="660a1-109">To polecenie tworzy Redisą pamięć podręczną dla przedsiębiorstw o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="660a1-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="660a1-110">Przykład 2: Tworzenie Redis pamięci podręcznej przedsiębiorstwa za pomocą opcjonalnych parametrów</span><span class="sxs-lookup"><span data-stu-id="660a1-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="660a1-111">To polecenie tworzy Redisą pamięć podręczną o nazwie mój bufor, korzystając z opcjonalnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="660a1-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="660a1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="660a1-112">PARAMETERS</span></span>

### <span data-ttu-id="660a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="660a1-113">-AsJob</span></span>
<span data-ttu-id="660a1-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="660a1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="660a1-115">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="660a1-115">-Capacity</span></span>
<span data-ttu-id="660a1-116">Rozmiar klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="660a1-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="660a1-117">Domyślna wartość 2 lub 3 w zależności od jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="660a1-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="660a1-118">Prawidłowymi wartościami są (2, 4, 6,...) dla wersji Enterprise SKU i (3, 9, 15,...) dla wersji Flash (wersje SKU).</span><span class="sxs-lookup"><span data-stu-id="660a1-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="660a1-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="660a1-119">-ClientProtocol</span></span>
<span data-ttu-id="660a1-120">Określa, czy klienci Redis mogą łączyć się przy użyciu protokołów szyfrowania TLS lub Redis.</span><span class="sxs-lookup"><span data-stu-id="660a1-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="660a1-121">Wartość domyślna to TLS-Encrypted.</span><span class="sxs-lookup"><span data-stu-id="660a1-121">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="660a1-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="660a1-122">-ClusteringPolicy</span></span>
<span data-ttu-id="660a1-123">Zasady klastrowania — domyślnie OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="660a1-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="660a1-124">Określone w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="660a1-124">Specified at create time.</span></span>

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

### <span data-ttu-id="660a1-125">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="660a1-125">-ClusterName</span></span>
<span data-ttu-id="660a1-126">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="660a1-126">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="660a1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660a1-127">-DefaultProfile</span></span>
<span data-ttu-id="660a1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="660a1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660a1-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="660a1-129">-EvictionPolicy</span></span>
<span data-ttu-id="660a1-130">Zasady wykluczania Redis-domyślnie VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="660a1-130">Redis eviction policy - default is VolatileLRU.</span></span>

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

### <span data-ttu-id="660a1-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="660a1-131">-Location</span></span>
<span data-ttu-id="660a1-132">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="660a1-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="660a1-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="660a1-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="660a1-134">Minimalna wersja protokołu TLS dla klastra do obsługi, na przykład 1,2</span><span class="sxs-lookup"><span data-stu-id="660a1-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

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

### <span data-ttu-id="660a1-135">-Module</span><span class="sxs-lookup"><span data-stu-id="660a1-135">-Module</span></span>
<span data-ttu-id="660a1-136">Opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="660a1-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="660a1-137">Aby skonstruować, zobacz sekcję notatki dla właściwości modułu i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="660a1-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="660a1-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="660a1-138">-NoWait</span></span>
<span data-ttu-id="660a1-139">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="660a1-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="660a1-140">-Port</span><span class="sxs-lookup"><span data-stu-id="660a1-140">-Port</span></span>
<span data-ttu-id="660a1-141">Port TCP punktu końcowego bazy danych.</span><span class="sxs-lookup"><span data-stu-id="660a1-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="660a1-142">Określone w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="660a1-142">Specified at create time.</span></span>
<span data-ttu-id="660a1-143">Domyślnie jest to dostępny port.</span><span class="sxs-lookup"><span data-stu-id="660a1-143">Defaults to an available port.</span></span>

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

### <span data-ttu-id="660a1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660a1-144">-ResourceGroupName</span></span>
<span data-ttu-id="660a1-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="660a1-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="660a1-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="660a1-146">-Sku</span></span>
<span data-ttu-id="660a1-147">Typ klastra RedisEnterprise do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="660a1-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="660a1-148">Możliwe wartości: (Enterprise_E10, EnterpriseFlash_F300 itd.)</span><span class="sxs-lookup"><span data-stu-id="660a1-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="660a1-149">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="660a1-149">-SubscriptionId</span></span>
<span data-ttu-id="660a1-150">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="660a1-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="660a1-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="660a1-151">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="660a1-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="660a1-152">-Tag</span></span>
<span data-ttu-id="660a1-153">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="660a1-153">Resource tags.</span></span>

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

### <span data-ttu-id="660a1-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="660a1-154">-Zone</span></span>
<span data-ttu-id="660a1-155">Strefy, w których zostanie wdrożony ten klaster.</span><span class="sxs-lookup"><span data-stu-id="660a1-155">The zones where this cluster will be deployed.</span></span>

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

### <span data-ttu-id="660a1-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="660a1-156">-Confirm</span></span>
<span data-ttu-id="660a1-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660a1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="660a1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660a1-158">-WhatIf</span></span>
<span data-ttu-id="660a1-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660a1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660a1-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="660a1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="660a1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660a1-161">CommonParameters</span></span>
<span data-ttu-id="660a1-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660a1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660a1-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="660a1-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660a1-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="660a1-164">INPUTS</span></span>

## <span data-ttu-id="660a1-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="660a1-165">OUTPUTS</span></span>

### <span data-ttu-id="660a1-166">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="660a1-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="660a1-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="660a1-167">NOTES</span></span>

<span data-ttu-id="660a1-168">PISUJE</span><span class="sxs-lookup"><span data-stu-id="660a1-168">ALIASES</span></span>

<span data-ttu-id="660a1-169">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="660a1-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="660a1-170">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="660a1-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="660a1-171">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="660a1-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="660a1-172">Moduł <IModule [] >: opcjonalny zestaw modułów Redis do włączenia w tej bazie danych może być dodawany tylko w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="660a1-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="660a1-173">`Name <String>`: Nazwa modułu, na przykład "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="660a1-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="660a1-174">`[Arg <String>]`: Opcje konfiguracji modułu, na przykład "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="660a1-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="660a1-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="660a1-175">RELATED LINKS</span></span>

