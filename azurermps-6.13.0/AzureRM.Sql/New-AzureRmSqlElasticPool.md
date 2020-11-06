---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544743"
---
# <span data-ttu-id="95d08-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95d08-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="95d08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95d08-102">SYNOPSIS</span></span>
<span data-ttu-id="95d08-103">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="95d08-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95d08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95d08-104">SYNTAX</span></span>

### <span data-ttu-id="95d08-105">DtuBasedPool (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95d08-105">DtuBasedPool (Default)</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d08-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="95d08-106">VcoreBasedPool</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d08-107">Opis</span><span class="sxs-lookup"><span data-stu-id="95d08-107">DESCRIPTION</span></span>
<span data-ttu-id="95d08-108">Polecenie cmdlet **New-AzureRmSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95d08-108">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="95d08-109">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="95d08-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="95d08-110">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="95d08-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="95d08-111">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="95d08-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="95d08-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95d08-112">EXAMPLES</span></span>

### <span data-ttu-id="95d08-113">Przykład 1. Tworzenie puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="95d08-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="95d08-114">To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="95d08-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="95d08-115">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="95d08-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="95d08-116">Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="95d08-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="95d08-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95d08-117">PARAMETERS</span></span>

### <span data-ttu-id="95d08-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95d08-118">-AsJob</span></span>
<span data-ttu-id="95d08-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="95d08-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95d08-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="95d08-120">-ComputeGeneration</span></span>
<span data-ttu-id="95d08-121">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="95d08-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="95d08-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="95d08-123">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="95d08-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="95d08-124">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="95d08-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="95d08-125">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="95d08-125">Basic.</span></span> <span data-ttu-id="95d08-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="95d08-126">5 DTUs</span></span>
- <span data-ttu-id="95d08-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="95d08-127">Standard.</span></span> <span data-ttu-id="95d08-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="95d08-128">100 DTUs</span></span>
- <span data-ttu-id="95d08-129">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="95d08-129">Premium.</span></span> <span data-ttu-id="95d08-130">125 DTU, aby uzyskać szczegółowe informacje dotyczące wartości, które są prawidłowe, można znaleźć w tabeli dotyczącej określonej puli rozmiarów w [pulach elastycznych](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="95d08-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="95d08-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="95d08-132">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="95d08-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="95d08-133">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="95d08-133">The default value is zero (0).</span></span>
<span data-ttu-id="95d08-134">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="95d08-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="95d08-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="95d08-136">Numer VCore Maxmium, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="95d08-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="95d08-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="95d08-138">Minimalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="95d08-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d08-139">-DefaultProfile</span></span>
<span data-ttu-id="95d08-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="95d08-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95d08-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="95d08-141">-Dtu</span></span>
<span data-ttu-id="95d08-142">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="95d08-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="95d08-143">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="95d08-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="95d08-144">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="95d08-144">Basic.</span></span>
<span data-ttu-id="95d08-145">100 DTU</span><span class="sxs-lookup"><span data-stu-id="95d08-145">100 DTUs</span></span>
- <span data-ttu-id="95d08-146">Standard.</span><span class="sxs-lookup"><span data-stu-id="95d08-146">Standard.</span></span>
<span data-ttu-id="95d08-147">100 DTU</span><span class="sxs-lookup"><span data-stu-id="95d08-147">100 DTUs</span></span>
- <span data-ttu-id="95d08-148">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="95d08-148">Premium.</span></span>
<span data-ttu-id="95d08-149">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="95d08-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="95d08-150">-Edition</span></span>
<span data-ttu-id="95d08-151">Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="95d08-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="95d08-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="95d08-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95d08-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="95d08-153">None</span></span>
- <span data-ttu-id="95d08-154">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="95d08-154">Basic</span></span>
- <span data-ttu-id="95d08-155">Standard</span><span class="sxs-lookup"><span data-stu-id="95d08-155">Standard</span></span>
- <span data-ttu-id="95d08-156">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="95d08-156">Premium</span></span>
- <span data-ttu-id="95d08-157">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="95d08-157">DataWarehouse</span></span>
- <span data-ttu-id="95d08-158">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="95d08-158">Free</span></span>
- <span data-ttu-id="95d08-159">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="95d08-159">Stretch</span></span>
- <span data-ttu-id="95d08-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="95d08-160">GeneralPurpose</span></span>
- <span data-ttu-id="95d08-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="95d08-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="95d08-162">-ElasticPoolName</span></span>
<span data-ttu-id="95d08-163">Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d08-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="95d08-164">-LicenseType</span></span>
<span data-ttu-id="95d08-165">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95d08-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="95d08-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d08-166">-ResourceGroupName</span></span>
<span data-ttu-id="95d08-167">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="95d08-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-168">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="95d08-168">-ServerName</span></span>
<span data-ttu-id="95d08-169">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="95d08-169">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="95d08-170">-StorageMB</span></span>
<span data-ttu-id="95d08-171">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="95d08-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="95d08-172">Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .</span><span class="sxs-lookup"><span data-stu-id="95d08-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="95d08-173">Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="95d08-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="95d08-174">-Tagi</span><span class="sxs-lookup"><span data-stu-id="95d08-174">-Tags</span></span>
<span data-ttu-id="95d08-175">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną.</span><span class="sxs-lookup"><span data-stu-id="95d08-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="95d08-176">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="95d08-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="95d08-177">-VCore</span></span>
<span data-ttu-id="95d08-178">Łączna przydzielona liczba Vcores dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95d08-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="95d08-179">-ZoneRedundant</span></span>
<span data-ttu-id="95d08-180">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="95d08-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="95d08-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95d08-181">-Confirm</span></span>
<span data-ttu-id="95d08-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d08-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d08-183">-WhatIf</span></span>
<span data-ttu-id="95d08-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d08-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d08-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95d08-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d08-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d08-186">CommonParameters</span></span>
<span data-ttu-id="95d08-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d08-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d08-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d08-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d08-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95d08-189">INPUTS</span></span>

### <span data-ttu-id="95d08-190">System. String</span><span class="sxs-lookup"><span data-stu-id="95d08-190">System.String</span></span>

## <span data-ttu-id="95d08-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95d08-191">OUTPUTS</span></span>

### <span data-ttu-id="95d08-192">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="95d08-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="95d08-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95d08-193">NOTES</span></span>

## <span data-ttu-id="95d08-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95d08-194">RELATED LINKS</span></span>

[<span data-ttu-id="95d08-195">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95d08-195">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="95d08-196">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="95d08-196">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="95d08-197">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="95d08-197">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="95d08-198">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95d08-198">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="95d08-199">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95d08-199">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="95d08-200">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="95d08-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
