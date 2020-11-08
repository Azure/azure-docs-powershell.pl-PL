---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225639"
---
# <span data-ttu-id="2dbfc-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2dbfc-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="2dbfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbfc-103">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="2dbfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dbfc-104">SYNTAX</span></span>

### <span data-ttu-id="2dbfc-105">DtuBasedPool (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2dbfc-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dbfc-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="2dbfc-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dbfc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2dbfc-107">DESCRIPTION</span></span>
<span data-ttu-id="2dbfc-108">Polecenie cmdlet **New-AzSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="2dbfc-109">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="2dbfc-110">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="2dbfc-111">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2dbfc-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="2dbfc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dbfc-112">EXAMPLES</span></span>

### <span data-ttu-id="2dbfc-113">Przykład 1. Tworzenie elastycznej puli jednostek DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="2dbfc-114">To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="2dbfc-115">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="2dbfc-116">Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="2dbfc-117">Przykład 2: Tworzenie elastycznej puli vCore</span><span class="sxs-lookup"><span data-stu-id="2dbfc-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
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

<span data-ttu-id="2dbfc-118">To polecenie tworzy elastyczną pulę w warstwie usług GengeralPurpose o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="2dbfc-119">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="2dbfc-120">Polecenie określa wartości właściwości vCore dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="2dbfc-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2dbfc-121">Example 3</span></span>

<span data-ttu-id="2dbfc-122">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="2dbfc-123">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="2dbfc-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="2dbfc-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dbfc-124">PARAMETERS</span></span>

### <span data-ttu-id="2dbfc-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dbfc-125">-AsJob</span></span>
<span data-ttu-id="2dbfc-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2dbfc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dbfc-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2dbfc-127">-ComputeGeneration</span></span>
<span data-ttu-id="2dbfc-128">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="2dbfc-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="2dbfc-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="2dbfc-130">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="2dbfc-131">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="2dbfc-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="2dbfc-132">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-132">Basic.</span></span> <span data-ttu-id="2dbfc-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-133">5 DTUs</span></span>
- <span data-ttu-id="2dbfc-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-134">Standard.</span></span> <span data-ttu-id="2dbfc-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-135">100 DTUs</span></span>
- <span data-ttu-id="2dbfc-136">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-136">Premium.</span></span> <span data-ttu-id="2dbfc-137">125 DTU, aby uzyskać szczegółowe informacje dotyczące wartości, które są prawidłowe, można znaleźć w tabeli dotyczącej określonej puli rozmiarów w [pulach elastycznych](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="2dbfc-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="2dbfc-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="2dbfc-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="2dbfc-139">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="2dbfc-140">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="2dbfc-140">The default value is zero (0).</span></span>
<span data-ttu-id="2dbfc-141">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2dbfc-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="2dbfc-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="2dbfc-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="2dbfc-143">Maksymalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="2dbfc-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="2dbfc-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="2dbfc-145">Minimalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="2dbfc-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbfc-146">-DefaultProfile</span></span>
<span data-ttu-id="2dbfc-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2dbfc-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dbfc-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-148">-Dtu</span></span>
<span data-ttu-id="2dbfc-149">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="2dbfc-150">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="2dbfc-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="2dbfc-151">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-151">Basic.</span></span>
<span data-ttu-id="2dbfc-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-152">100 DTUs</span></span>
- <span data-ttu-id="2dbfc-153">Standard.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-153">Standard.</span></span>
<span data-ttu-id="2dbfc-154">100 DTU</span><span class="sxs-lookup"><span data-stu-id="2dbfc-154">100 DTUs</span></span>
- <span data-ttu-id="2dbfc-155">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-155">Premium.</span></span>
<span data-ttu-id="2dbfc-156">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2dbfc-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="2dbfc-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="2dbfc-157">-Edition</span></span>
<span data-ttu-id="2dbfc-158">Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="2dbfc-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2dbfc-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2dbfc-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2dbfc-160">None</span></span>
- <span data-ttu-id="2dbfc-161">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="2dbfc-161">Basic</span></span>
- <span data-ttu-id="2dbfc-162">Standard</span><span class="sxs-lookup"><span data-stu-id="2dbfc-162">Standard</span></span>
- <span data-ttu-id="2dbfc-163">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="2dbfc-163">Premium</span></span>
- <span data-ttu-id="2dbfc-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2dbfc-164">DataWarehouse</span></span>
- <span data-ttu-id="2dbfc-165">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="2dbfc-165">Free</span></span>
- <span data-ttu-id="2dbfc-166">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="2dbfc-166">Stretch</span></span>
- <span data-ttu-id="2dbfc-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="2dbfc-167">GeneralPurpose</span></span>
- <span data-ttu-id="2dbfc-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2dbfc-168">BusinessCritical</span></span>

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

### <span data-ttu-id="2dbfc-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2dbfc-169">-ElasticPoolName</span></span>
<span data-ttu-id="2dbfc-170">Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2dbfc-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2dbfc-171">-LicenseType</span></span>
<span data-ttu-id="2dbfc-172">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="2dbfc-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbfc-173">-ResourceGroupName</span></span>
<span data-ttu-id="2dbfc-174">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="2dbfc-175">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2dbfc-175">-ServerName</span></span>
<span data-ttu-id="2dbfc-176">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="2dbfc-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="2dbfc-177">-StorageMB</span></span>
<span data-ttu-id="2dbfc-178">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="2dbfc-179">Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .</span><span class="sxs-lookup"><span data-stu-id="2dbfc-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="2dbfc-180">Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="2dbfc-181">-Tagi</span><span class="sxs-lookup"><span data-stu-id="2dbfc-181">-Tags</span></span>
<span data-ttu-id="2dbfc-182">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="2dbfc-183">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="2dbfc-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2dbfc-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="2dbfc-184">-VCore</span></span>
<span data-ttu-id="2dbfc-185">Łączna przydzielona liczba Vcores dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="2dbfc-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2dbfc-186">-ZoneRedundant</span></span>
<span data-ttu-id="2dbfc-187">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="2dbfc-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="2dbfc-188">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dbfc-188">-Confirm</span></span>
<span data-ttu-id="2dbfc-189">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dbfc-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dbfc-190">-WhatIf</span></span>
<span data-ttu-id="2dbfc-191">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dbfc-192">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dbfc-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbfc-193">CommonParameters</span></span>
<span data-ttu-id="2dbfc-194">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbfc-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbfc-195">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dbfc-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbfc-196">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dbfc-196">INPUTS</span></span>

### <span data-ttu-id="2dbfc-197">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbfc-197">System.String</span></span>

## <span data-ttu-id="2dbfc-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dbfc-198">OUTPUTS</span></span>

### <span data-ttu-id="2dbfc-199">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="2dbfc-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="2dbfc-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dbfc-200">NOTES</span></span>

## <span data-ttu-id="2dbfc-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dbfc-201">RELATED LINKS</span></span>

[<span data-ttu-id="2dbfc-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2dbfc-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2dbfc-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2dbfc-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="2dbfc-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2dbfc-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2dbfc-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2dbfc-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2dbfc-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2dbfc-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="2dbfc-207">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2dbfc-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
