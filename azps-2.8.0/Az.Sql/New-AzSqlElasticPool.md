---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: f16313710e0ab007f23df0cfa3a2214f78a8963a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886845"
---
# <span data-ttu-id="27b9c-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27b9c-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="27b9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="27b9c-103">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="27b9c-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="27b9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27b9c-104">SYNTAX</span></span>

### <span data-ttu-id="27b9c-105">DtuBasedPool (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27b9c-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27b9c-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="27b9c-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b9c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="27b9c-107">DESCRIPTION</span></span>
<span data-ttu-id="27b9c-108">Polecenie cmdlet **New-AzSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27b9c-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="27b9c-109">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="27b9c-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="27b9c-110">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="27b9c-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="27b9c-111">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="27b9c-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="27b9c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27b9c-112">EXAMPLES</span></span>

### <span data-ttu-id="27b9c-113">Przykład 1. Tworzenie elastycznej puli jednostek DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-113">Example 1: Create a DTU elastic pool</span></span>

```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="27b9c-114">To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="27b9c-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="27b9c-115">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="27b9c-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="27b9c-116">Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="27b9c-117">Przykład 2: Tworzenie elastycznej puli vCore</span><span class="sxs-lookup"><span data-stu-id="27b9c-117">Example 2: Create a vCore elastic pool</span></span>

```
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                : 
```


<span data-ttu-id="27b9c-118">To polecenie tworzy elastyczną pulę w warstwie usług GengeralPurpose o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="27b9c-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="27b9c-119">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="27b9c-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="27b9c-120">Polecenie określa wartości właściwości vCore dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="27b9c-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27b9c-121">PARAMETERS</span></span>

### <span data-ttu-id="27b9c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27b9c-122">-AsJob</span></span>
<span data-ttu-id="27b9c-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="27b9c-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27b9c-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="27b9c-124">-ComputeGeneration</span></span>
<span data-ttu-id="27b9c-125">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="27b9c-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="27b9c-126">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="27b9c-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="27b9c-127">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="27b9c-128">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="27b9c-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="27b9c-129">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="27b9c-129">Basic.</span></span> <span data-ttu-id="27b9c-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-130">5 DTUs</span></span>
- <span data-ttu-id="27b9c-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="27b9c-131">Standard.</span></span> <span data-ttu-id="27b9c-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-132">100 DTUs</span></span>
- <span data-ttu-id="27b9c-133">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="27b9c-133">Premium.</span></span> <span data-ttu-id="27b9c-134">125 DTU, aby uzyskać szczegółowe informacje dotyczące wartości, które są prawidłowe, można znaleźć w tabeli dotyczącej określonej puli rozmiarów w [pulach elastycznych](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="27b9c-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="27b9c-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="27b9c-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="27b9c-136">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="27b9c-137">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="27b9c-137">The default value is zero (0).</span></span>
<span data-ttu-id="27b9c-138">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="27b9c-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="27b9c-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="27b9c-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="27b9c-140">Maksymalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="27b9c-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="27b9c-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="27b9c-142">Minimalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="27b9c-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="27b9c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b9c-143">-DefaultProfile</span></span>
<span data-ttu-id="27b9c-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="27b9c-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27b9c-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-145">-Dtu</span></span>
<span data-ttu-id="27b9c-146">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="27b9c-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="27b9c-147">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="27b9c-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="27b9c-148">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="27b9c-148">Basic.</span></span>
<span data-ttu-id="27b9c-149">100 DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-149">100 DTUs</span></span>
- <span data-ttu-id="27b9c-150">Standard.</span><span class="sxs-lookup"><span data-stu-id="27b9c-150">Standard.</span></span>
<span data-ttu-id="27b9c-151">100 DTU</span><span class="sxs-lookup"><span data-stu-id="27b9c-151">100 DTUs</span></span>
- <span data-ttu-id="27b9c-152">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="27b9c-152">Premium.</span></span>
<span data-ttu-id="27b9c-153">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="27b9c-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="27b9c-154">-Edition</span><span class="sxs-lookup"><span data-stu-id="27b9c-154">-Edition</span></span>
<span data-ttu-id="27b9c-155">Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="27b9c-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="27b9c-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27b9c-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27b9c-157">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="27b9c-157">None</span></span>
- <span data-ttu-id="27b9c-158">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="27b9c-158">Basic</span></span>
- <span data-ttu-id="27b9c-159">Standard</span><span class="sxs-lookup"><span data-stu-id="27b9c-159">Standard</span></span>
- <span data-ttu-id="27b9c-160">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="27b9c-160">Premium</span></span>
- <span data-ttu-id="27b9c-161">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="27b9c-161">DataWarehouse</span></span>
- <span data-ttu-id="27b9c-162">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="27b9c-162">Free</span></span>
- <span data-ttu-id="27b9c-163">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="27b9c-163">Stretch</span></span>
- <span data-ttu-id="27b9c-164">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="27b9c-164">GeneralPurpose</span></span>
- <span data-ttu-id="27b9c-165">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="27b9c-165">BusinessCritical</span></span>

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

### <span data-ttu-id="27b9c-166">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="27b9c-166">-ElasticPoolName</span></span>
<span data-ttu-id="27b9c-167">Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b9c-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="27b9c-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="27b9c-168">-LicenseType</span></span>
<span data-ttu-id="27b9c-169">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27b9c-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="27b9c-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b9c-170">-ResourceGroupName</span></span>
<span data-ttu-id="27b9c-171">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="27b9c-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="27b9c-172">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="27b9c-172">-ServerName</span></span>
<span data-ttu-id="27b9c-173">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="27b9c-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="27b9c-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="27b9c-174">-StorageMB</span></span>
<span data-ttu-id="27b9c-175">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="27b9c-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="27b9c-176">Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .</span><span class="sxs-lookup"><span data-stu-id="27b9c-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="27b9c-177">Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="27b9c-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="27b9c-178">-Tagi</span><span class="sxs-lookup"><span data-stu-id="27b9c-178">-Tags</span></span>
<span data-ttu-id="27b9c-179">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną.</span><span class="sxs-lookup"><span data-stu-id="27b9c-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="27b9c-180">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="27b9c-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="27b9c-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="27b9c-181">-VCore</span></span>
<span data-ttu-id="27b9c-182">Łączna przydzielona liczba Vcores dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27b9c-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="27b9c-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="27b9c-183">-ZoneRedundant</span></span>
<span data-ttu-id="27b9c-184">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="27b9c-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="27b9c-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27b9c-185">-Confirm</span></span>
<span data-ttu-id="27b9c-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b9c-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b9c-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b9c-187">-WhatIf</span></span>
<span data-ttu-id="27b9c-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b9c-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b9c-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27b9c-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b9c-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b9c-190">CommonParameters</span></span>
<span data-ttu-id="27b9c-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b9c-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b9c-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27b9c-192">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b9c-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27b9c-193">INPUTS</span></span>

### <span data-ttu-id="27b9c-194">System. String</span><span class="sxs-lookup"><span data-stu-id="27b9c-194">System.String</span></span>

## <span data-ttu-id="27b9c-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27b9c-195">OUTPUTS</span></span>

### <span data-ttu-id="27b9c-196">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="27b9c-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="27b9c-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27b9c-197">NOTES</span></span>

## <span data-ttu-id="27b9c-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27b9c-198">RELATED LINKS</span></span>

[<span data-ttu-id="27b9c-199">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27b9c-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="27b9c-200">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="27b9c-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="27b9c-201">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="27b9c-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="27b9c-202">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27b9c-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="27b9c-203">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="27b9c-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="27b9c-204">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="27b9c-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
