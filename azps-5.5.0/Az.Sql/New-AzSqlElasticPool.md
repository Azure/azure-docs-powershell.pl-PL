---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 64234421f7507bb77511f136efe60657f439228f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191011"
---
# <span data-ttu-id="5f30b-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5f30b-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="5f30b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f30b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f30b-103">Tworzy elastyczną pulę baz danych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f30b-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="5f30b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f30b-104">SYNTAX</span></span>

### <span data-ttu-id="5f30b-105">DtuBasedPool (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5f30b-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f30b-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="5f30b-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f30b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f30b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f30b-108">Polecenie **cmdlet New-AzSqlElasticPool** tworzy elastyczną pulę baz danych dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5f30b-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="5f30b-109">Kilka parametrów *(-Dtu, -DatabaseDtuMin i -DatabaseDtuMax)* wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="5f30b-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="5f30b-110">Na przykład wartość -DatabaseDtuMax dla puli eDTU Standard 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="5f30b-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="5f30b-111">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5f30b-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="5f30b-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f30b-112">EXAMPLES</span></span>

### <span data-ttu-id="5f30b-113">Przykład 1. Tworzenie puli elastycznej DTU</span><span class="sxs-lookup"><span data-stu-id="5f30b-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="5f30b-114">To polecenie tworzy elastyczną pulę w warstwie Usługi standardowej o nazwie 2001.</span><span class="sxs-lookup"><span data-stu-id="5f30b-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="5f30b-115">Serwer o nazwie serwer01 przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01 hostuje elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="5f30b-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="5f30b-116">To polecenie określa wartości właściwości DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="5f30b-117">Przykład 2. Tworzenie elastycznej puli procesorów vCore</span><span class="sxs-lookup"><span data-stu-id="5f30b-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="5f30b-118">To polecenie tworzy elastyczną pulę w warstwie usługi GengeralPurpose o nazwie 1.</span><span class="sxs-lookup"><span data-stu-id="5f30b-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="5f30b-119">Serwer o nazwie serwer01 przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01 hostuje elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="5f30b-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="5f30b-120">To polecenie określa wartości właściwości vCore puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="5f30b-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5f30b-121">Example 3</span></span>

<span data-ttu-id="5f30b-122">Tworzy elastyczną pulę baz danych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f30b-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="5f30b-123">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="5f30b-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="5f30b-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f30b-124">PARAMETERS</span></span>

### <span data-ttu-id="5f30b-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5f30b-125">-AsJob</span></span>
<span data-ttu-id="5f30b-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5f30b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f30b-127">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="5f30b-127">-ComputeGeneration</span></span>
<span data-ttu-id="5f30b-128">Generowanie obliczeniowe do przypisania.</span><span class="sxs-lookup"><span data-stu-id="5f30b-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5f30b-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="5f30b-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="5f30b-130">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), z których może korzystać każda pojedyncza baza danych w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="5f30b-131">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="5f30b-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="5f30b-132">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="5f30b-132">Basic.</span></span> <span data-ttu-id="5f30b-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="5f30b-133">5 DTUs</span></span>
- <span data-ttu-id="5f30b-134">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="5f30b-134">Standard.</span></span> <span data-ttu-id="5f30b-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="5f30b-135">100 DTUs</span></span>
- <span data-ttu-id="5f30b-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="5f30b-136">Premium.</span></span> <span data-ttu-id="5f30b-137">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5f30b-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="5f30b-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="5f30b-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="5f30b-139">Określa minimalną liczbę jednostek DTU, które elastyczna pula gwarantuje wszystkim bazom danych w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="5f30b-140">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="5f30b-140">The default value is zero (0).</span></span>
<span data-ttu-id="5f30b-141">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5f30b-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="5f30b-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="5f30b-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="5f30b-143">Maksymalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5f30b-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="5f30b-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="5f30b-145">Minimalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="5f30b-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5f30b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f30b-146">-DefaultProfile</span></span>
<span data-ttu-id="5f30b-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5f30b-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f30b-148">- Dtu</span><span class="sxs-lookup"><span data-stu-id="5f30b-148">-Dtu</span></span>
<span data-ttu-id="5f30b-149">Określa całkowitą liczbę współużytkonych jednostek DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5f30b-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="5f30b-150">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="5f30b-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="5f30b-151">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="5f30b-151">Basic.</span></span>
<span data-ttu-id="5f30b-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="5f30b-152">100 DTUs</span></span>
- <span data-ttu-id="5f30b-153">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="5f30b-153">Standard.</span></span>
<span data-ttu-id="5f30b-154">100 DTU</span><span class="sxs-lookup"><span data-stu-id="5f30b-154">100 DTUs</span></span>
- <span data-ttu-id="5f30b-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="5f30b-155">Premium.</span></span>
<span data-ttu-id="5f30b-156">125 DTU Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5f30b-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="5f30b-157">— wersja</span><span class="sxs-lookup"><span data-stu-id="5f30b-157">-Edition</span></span>
<span data-ttu-id="5f30b-158">Określa wersję bazy danych Azure SQL Database używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5f30b-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="5f30b-159">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f30b-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5f30b-160">Brak</span><span class="sxs-lookup"><span data-stu-id="5f30b-160">None</span></span>
- <span data-ttu-id="5f30b-161">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="5f30b-161">Basic</span></span>
- <span data-ttu-id="5f30b-162">Standardowe</span><span class="sxs-lookup"><span data-stu-id="5f30b-162">Standard</span></span>
- <span data-ttu-id="5f30b-163">Premium</span><span class="sxs-lookup"><span data-stu-id="5f30b-163">Premium</span></span>
- <span data-ttu-id="5f30b-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5f30b-164">DataWarehouse</span></span>
- <span data-ttu-id="5f30b-165">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="5f30b-165">Free</span></span>
- <span data-ttu-id="5f30b-166">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="5f30b-166">Stretch</span></span>
- <span data-ttu-id="5f30b-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="5f30b-167">GeneralPurpose</span></span>
- <span data-ttu-id="5f30b-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5f30b-168">BusinessCritical</span></span>

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

### <span data-ttu-id="5f30b-169">-PochylićPoolName</span><span class="sxs-lookup"><span data-stu-id="5f30b-169">-ElasticPoolName</span></span>
<span data-ttu-id="5f30b-170">Określa nazwę puli elastycznej, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f30b-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5f30b-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5f30b-171">-LicenseType</span></span>
<span data-ttu-id="5f30b-172">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="5f30b-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5f30b-173">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5f30b-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="5f30b-174">Identyfikator konfiguracji konserwacji puli elastycznej SQL.</span><span class="sxs-lookup"><span data-stu-id="5f30b-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="5f30b-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f30b-175">-ResourceGroupName</span></span>
<span data-ttu-id="5f30b-176">Określa nazwę grupy zasobów, do której to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="5f30b-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="5f30b-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5f30b-177">-ServerName</span></span>
<span data-ttu-id="5f30b-178">Określa nazwę serwera hostowego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="5f30b-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5f30b-179">— StorageMB</span><span class="sxs-lookup"><span data-stu-id="5f30b-179">-StorageMB</span></span>
<span data-ttu-id="5f30b-180">Określa limit magazynowania puli elastycznej (w megabajtach).</span><span class="sxs-lookup"><span data-stu-id="5f30b-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="5f30b-181">Jeśli nie określisz tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości *parametru Dtu.*</span><span class="sxs-lookup"><span data-stu-id="5f30b-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="5f30b-182">Zobacz [informacje o eDTU i limitach magazynowania,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) aby uzyskać informacje o możliwych wartościach.</span><span class="sxs-lookup"><span data-stu-id="5f30b-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="5f30b-183">— Tagi</span><span class="sxs-lookup"><span data-stu-id="5f30b-183">-Tags</span></span>
<span data-ttu-id="5f30b-184">Określa słownik par klucz-wartość w postaci tabeli skrótu, który to polecenie cmdlet skojarzy z elastyczną pulą.</span><span class="sxs-lookup"><span data-stu-id="5f30b-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="5f30b-185">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5f30b-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5f30b-186">— VCore</span><span class="sxs-lookup"><span data-stu-id="5f30b-186">-VCore</span></span>
<span data-ttu-id="5f30b-187">Całkowita udostępniona liczba procesorów Vcore dla puli elastycznej platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="5f30b-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="5f30b-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5f30b-188">-ZoneRedundant</span></span>
<span data-ttu-id="5f30b-189">Nadmiarowość stref, która ma być skojarzana z pulą azure sql i elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="5f30b-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="5f30b-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f30b-190">-Confirm</span></span>
<span data-ttu-id="5f30b-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f30b-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f30b-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f30b-192">-WhatIf</span></span>
<span data-ttu-id="5f30b-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f30b-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f30b-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5f30b-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f30b-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f30b-195">CommonParameters</span></span>
<span data-ttu-id="5f30b-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f30b-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f30b-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f30b-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f30b-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f30b-198">INPUTS</span></span>

### <span data-ttu-id="5f30b-199">System.String</span><span class="sxs-lookup"><span data-stu-id="5f30b-199">System.String</span></span>

## <span data-ttu-id="5f30b-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f30b-200">OUTPUTS</span></span>

### <span data-ttu-id="5f30b-201">Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="5f30b-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5f30b-202">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f30b-202">NOTES</span></span>

## <span data-ttu-id="5f30b-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f30b-203">RELATED LINKS</span></span>

[<span data-ttu-id="5f30b-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5f30b-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="5f30b-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5f30b-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="5f30b-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5f30b-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="5f30b-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5f30b-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="5f30b-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5f30b-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="5f30b-209">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5f30b-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
