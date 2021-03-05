---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970209"
---
# <span data-ttu-id="93f34-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93f34-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="93f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f34-102">SYNOPSIS</span></span>
<span data-ttu-id="93f34-103">Tworzy elastyczną pulę baz danych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="93f34-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="93f34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93f34-104">SYNTAX</span></span>

### <span data-ttu-id="93f34-105">DtuBasedPool (domyślne)</span><span class="sxs-lookup"><span data-stu-id="93f34-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93f34-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="93f34-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f34-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="93f34-107">DESCRIPTION</span></span>
<span data-ttu-id="93f34-108">Polecenie **cmdlet New-AzSqlElasticPool** tworzy elastyczną pulę baz danych dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="93f34-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="93f34-109">Kilka parametrów *(-Dtu, -DatabaseDtuMin i -DatabaseDtuMax)* wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="93f34-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="93f34-110">Na przykład wartość -DatabaseDtuMax dla puli eDTU Standard 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="93f34-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="93f34-111">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="93f34-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="93f34-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93f34-112">EXAMPLES</span></span>

### <span data-ttu-id="93f34-113">Przykład 1. Tworzenie puli elastycznej DTU</span><span class="sxs-lookup"><span data-stu-id="93f34-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="93f34-114">To polecenie tworzy elastyczną pulę w warstwie Usługi standardowej o nazwie 1000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="93f34-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="93f34-115">Serwer o nazwie serwer01 przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01 hostuje elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="93f34-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="93f34-116">To polecenie określa wartości właściwości dtu dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="93f34-117">Przykład 2. Tworzenie puli elastycznej z procesorem vCore</span><span class="sxs-lookup"><span data-stu-id="93f34-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="93f34-118">To polecenie tworzy elastyczną pulę w warstwie usługi GengeralPurpose o nazwie 1.</span><span class="sxs-lookup"><span data-stu-id="93f34-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="93f34-119">Serwer o nazwie serwer01 przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01 hostuje elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="93f34-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="93f34-120">To polecenie określa wartości właściwości vCore puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="93f34-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="93f34-121">Example 3</span></span>

<span data-ttu-id="93f34-122">Tworzy elastyczną pulę baz danych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="93f34-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="93f34-123">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="93f34-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="93f34-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f34-124">PARAMETERS</span></span>

### <span data-ttu-id="93f34-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="93f34-125">-AsJob</span></span>
<span data-ttu-id="93f34-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="93f34-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93f34-127">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="93f34-127">-ComputeGeneration</span></span>
<span data-ttu-id="93f34-128">Generowanie obliczeniowe do przypisania.</span><span class="sxs-lookup"><span data-stu-id="93f34-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="93f34-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="93f34-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="93f34-130">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), z których może korzystać każda pojedyncza baza danych w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="93f34-131">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="93f34-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="93f34-132">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="93f34-132">Basic.</span></span> <span data-ttu-id="93f34-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="93f34-133">5 DTUs</span></span>
- <span data-ttu-id="93f34-134">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="93f34-134">Standard.</span></span> <span data-ttu-id="93f34-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="93f34-135">100 DTUs</span></span>
- <span data-ttu-id="93f34-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="93f34-136">Premium.</span></span> <span data-ttu-id="93f34-137">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="93f34-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="93f34-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="93f34-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="93f34-139">Określa minimalną liczbę jednostek DTU, które elastyczna pula gwarantuje wszystkim bazom danych w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="93f34-140">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="93f34-140">The default value is zero (0).</span></span>
<span data-ttu-id="93f34-141">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="93f34-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="93f34-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="93f34-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="93f34-143">Maksymalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="93f34-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="93f34-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="93f34-145">Minimalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="93f34-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="93f34-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f34-146">-DefaultProfile</span></span>
<span data-ttu-id="93f34-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="93f34-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f34-148">- Dtu</span><span class="sxs-lookup"><span data-stu-id="93f34-148">-Dtu</span></span>
<span data-ttu-id="93f34-149">Określa całkowitą liczbę współużytkonych jednostek DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="93f34-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="93f34-150">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="93f34-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="93f34-151">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="93f34-151">Basic.</span></span>
<span data-ttu-id="93f34-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="93f34-152">100 DTUs</span></span>
- <span data-ttu-id="93f34-153">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="93f34-153">Standard.</span></span>
<span data-ttu-id="93f34-154">100 DTU</span><span class="sxs-lookup"><span data-stu-id="93f34-154">100 DTUs</span></span>
- <span data-ttu-id="93f34-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="93f34-155">Premium.</span></span>
<span data-ttu-id="93f34-156">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="93f34-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="93f34-157">— wersja</span><span class="sxs-lookup"><span data-stu-id="93f34-157">-Edition</span></span>
<span data-ttu-id="93f34-158">Określa wersję bazy danych Azure SQL Database używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="93f34-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="93f34-159">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="93f34-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93f34-160">Brak</span><span class="sxs-lookup"><span data-stu-id="93f34-160">None</span></span>
- <span data-ttu-id="93f34-161">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="93f34-161">Basic</span></span>
- <span data-ttu-id="93f34-162">Standardowe</span><span class="sxs-lookup"><span data-stu-id="93f34-162">Standard</span></span>
- <span data-ttu-id="93f34-163">Premium</span><span class="sxs-lookup"><span data-stu-id="93f34-163">Premium</span></span>
- <span data-ttu-id="93f34-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="93f34-164">DataWarehouse</span></span>
- <span data-ttu-id="93f34-165">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="93f34-165">Free</span></span>
- <span data-ttu-id="93f34-166">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="93f34-166">Stretch</span></span>
- <span data-ttu-id="93f34-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="93f34-167">GeneralPurpose</span></span>
- <span data-ttu-id="93f34-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="93f34-168">BusinessCritical</span></span>

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

### <span data-ttu-id="93f34-169">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="93f34-169">-ElasticPoolName</span></span>
<span data-ttu-id="93f34-170">Określa nazwę puli elastycznej, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93f34-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="93f34-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="93f34-171">-LicenseType</span></span>
<span data-ttu-id="93f34-172">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="93f34-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="93f34-173">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="93f34-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="93f34-174">Identyfikator konfiguracji konserwacji puli elastycznej SQL.</span><span class="sxs-lookup"><span data-stu-id="93f34-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="93f34-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f34-175">-ResourceGroupName</span></span>
<span data-ttu-id="93f34-176">Określa nazwę grupy zasobów, do której to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="93f34-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="93f34-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93f34-177">-ServerName</span></span>
<span data-ttu-id="93f34-178">Określa nazwę serwera hostowego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="93f34-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="93f34-179">— StorageMB</span><span class="sxs-lookup"><span data-stu-id="93f34-179">-StorageMB</span></span>
<span data-ttu-id="93f34-180">Określa limit magazynowania puli elastycznej (w megabajtach).</span><span class="sxs-lookup"><span data-stu-id="93f34-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="93f34-181">Jeśli nie określisz tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości *parametru Dtu.*</span><span class="sxs-lookup"><span data-stu-id="93f34-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="93f34-182">Zobacz [informacje o eDTU i limitach magazynowania, aby](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) uzyskać informacje o możliwych wartościach.</span><span class="sxs-lookup"><span data-stu-id="93f34-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="93f34-183">— Tagi</span><span class="sxs-lookup"><span data-stu-id="93f34-183">-Tags</span></span>
<span data-ttu-id="93f34-184">Określa słownik par klucz-wartość w postaci tabeli skrótu, który to polecenie cmdlet skojarzy z elastyczną pulą.</span><span class="sxs-lookup"><span data-stu-id="93f34-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="93f34-185">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="93f34-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93f34-186">— VCore</span><span class="sxs-lookup"><span data-stu-id="93f34-186">-VCore</span></span>
<span data-ttu-id="93f34-187">Całkowita udostępniona liczba procesorów Vcore dla puli elastycznej platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="93f34-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="93f34-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="93f34-188">-ZoneRedundant</span></span>
<span data-ttu-id="93f34-189">Nadmiarowość stref, która ma być skojarzana z pulą Azure Sql 2010</span><span class="sxs-lookup"><span data-stu-id="93f34-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="93f34-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93f34-190">-Confirm</span></span>
<span data-ttu-id="93f34-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93f34-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f34-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f34-192">-WhatIf</span></span>
<span data-ttu-id="93f34-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93f34-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f34-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93f34-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f34-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f34-195">CommonParameters</span></span>
<span data-ttu-id="93f34-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f34-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f34-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93f34-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f34-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93f34-198">INPUTS</span></span>

### <span data-ttu-id="93f34-199">System.String</span><span class="sxs-lookup"><span data-stu-id="93f34-199">System.String</span></span>

## <span data-ttu-id="93f34-200">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93f34-200">OUTPUTS</span></span>

### <span data-ttu-id="93f34-201">Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="93f34-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="93f34-202">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93f34-202">NOTES</span></span>

## <span data-ttu-id="93f34-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93f34-203">RELATED LINKS</span></span>

[<span data-ttu-id="93f34-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93f34-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="93f34-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="93f34-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="93f34-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="93f34-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="93f34-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93f34-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="93f34-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93f34-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="93f34-209">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="93f34-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
