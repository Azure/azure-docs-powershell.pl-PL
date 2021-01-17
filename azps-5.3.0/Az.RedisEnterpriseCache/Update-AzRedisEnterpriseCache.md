---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378170"
---
# <span data-ttu-id="29328-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="29328-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="29328-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29328-102">SYNOPSIS</span></span>
<span data-ttu-id="29328-103">Aktualizuje istniejący klaster RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="29328-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="29328-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29328-104">SYNTAX</span></span>

### <span data-ttu-id="29328-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29328-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29328-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29328-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29328-107">Opis</span><span class="sxs-lookup"><span data-stu-id="29328-107">DESCRIPTION</span></span>
<span data-ttu-id="29328-108">Aktualizuje istniejący klaster RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="29328-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="29328-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29328-109">EXAMPLES</span></span>

### <span data-ttu-id="29328-110">Przykład 1: Aktualizacja pamięci podręcznej w usłudze Redis Enterprise</span><span class="sxs-lookup"><span data-stu-id="29328-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="29328-111">To polecenie powoduje zaktualizowanie minimalnej wersji protokołu TLS i dodanie znacznika do pamięci podręcznej Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="29328-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="29328-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29328-112">PARAMETERS</span></span>

### <span data-ttu-id="29328-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29328-113">-AsJob</span></span>
<span data-ttu-id="29328-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="29328-114">Run the command as a job</span></span>

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

### <span data-ttu-id="29328-115">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="29328-115">-Capacity</span></span>
<span data-ttu-id="29328-116">Rozmiar klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="29328-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="29328-117">Domyślna wartość 2 lub 3 w zależności od jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="29328-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="29328-118">Prawidłowymi wartościami są (2, 4, 6,...) dla wersji Enterprise SKU i (3, 9, 15,...) dla wersji Flash (wersje SKU).</span><span class="sxs-lookup"><span data-stu-id="29328-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="29328-119">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="29328-119">-ClusterName</span></span>
<span data-ttu-id="29328-120">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="29328-120">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29328-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29328-121">-DefaultProfile</span></span>
<span data-ttu-id="29328-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29328-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29328-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29328-123">-InputObject</span></span>
<span data-ttu-id="29328-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="29328-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29328-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="29328-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="29328-126">Minimalna wersja protokołu TLS dla klastra do obsługi, na przykład "1,2"</span><span class="sxs-lookup"><span data-stu-id="29328-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="29328-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="29328-127">-NoWait</span></span>
<span data-ttu-id="29328-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="29328-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29328-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29328-129">-ResourceGroupName</span></span>
<span data-ttu-id="29328-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29328-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29328-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="29328-131">-Sku</span></span>
<span data-ttu-id="29328-132">Typ klastra RedisEnterprise do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="29328-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="29328-133">Możliwe wartości: (Enterprise_E10, EnterpriseFlash_F300 itd.)</span><span class="sxs-lookup"><span data-stu-id="29328-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29328-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29328-134">-SubscriptionId</span></span>
<span data-ttu-id="29328-135">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="29328-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="29328-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="29328-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29328-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="29328-137">-Tag</span></span>
<span data-ttu-id="29328-138">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="29328-138">Resource tags.</span></span>

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

### <span data-ttu-id="29328-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29328-139">-Confirm</span></span>
<span data-ttu-id="29328-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29328-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29328-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29328-141">-WhatIf</span></span>
<span data-ttu-id="29328-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29328-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29328-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29328-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29328-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29328-144">CommonParameters</span></span>
<span data-ttu-id="29328-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29328-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29328-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29328-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29328-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29328-147">INPUTS</span></span>

### <span data-ttu-id="29328-148">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="29328-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="29328-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29328-149">OUTPUTS</span></span>

### <span data-ttu-id="29328-150">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="29328-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="29328-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29328-151">NOTES</span></span>

<span data-ttu-id="29328-152">PISUJE</span><span class="sxs-lookup"><span data-stu-id="29328-152">ALIASES</span></span>

<span data-ttu-id="29328-153">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29328-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29328-154">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="29328-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29328-155">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29328-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29328-156">INPUTobject <IRedisEnterpriseCacheIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="29328-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29328-157">`[ClusterName <String>]`: Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="29328-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="29328-158">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="29328-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="29328-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="29328-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29328-160">`[Location <String>]`: Region, w którym znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="29328-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="29328-161">`[OperationId <String>]`: Unikatowy identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="29328-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="29328-162">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="29328-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="29328-163">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29328-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="29328-164">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="29328-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="29328-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="29328-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="29328-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29328-166">RELATED LINKS</span></span>

