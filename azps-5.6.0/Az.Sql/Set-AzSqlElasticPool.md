---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963601"
---
# <span data-ttu-id="332b3-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="332b3-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="332b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="332b3-102">SYNOPSIS</span></span>
<span data-ttu-id="332b3-103">Modyfikuje właściwości elastycznej puli baz danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="332b3-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="332b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="332b3-104">SYNTAX</span></span>

### <span data-ttu-id="332b3-105">DtuBasedPool (domyślne)</span><span class="sxs-lookup"><span data-stu-id="332b3-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="332b3-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="332b3-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="332b3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="332b3-107">DESCRIPTION</span></span>
<span data-ttu-id="332b3-108">Polecenie **cmdlet Set-AzSqlElasticPool** ustawia właściwości elastycznej puli w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="332b3-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="332b3-109">To polecenie cmdlet może modyfikować wartości eDTU na pulę *(Dtu),* maksymalny rozmiar przestrzeni dyskowej na pulę *(StorageMB),* maksymalna liczba jednostek eDTU na bazę danych *(DatabaseDtuMax)* oraz minimalne liczby eDTU na bazę danych *(DatabaseDtuMin).*</span><span class="sxs-lookup"><span data-stu-id="332b3-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="332b3-110">Kilka parametrów *(-Dtu, -DatabaseDtuMin i -DatabaseDtuMax)* wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="332b3-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="332b3-111">Na przykład wartość -DatabaseDtuMax dla puli eDTU Standard 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="332b3-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="332b3-112">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="332b3-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="332b3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="332b3-113">EXAMPLES</span></span>

### <span data-ttu-id="332b3-114">Przykład 1. Modyfikowanie właściwości puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="332b3-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="332b3-115">To polecenie modyfikuje właściwości puli elastycznej o nazwiePoolpool01.</span><span class="sxs-lookup"><span data-stu-id="332b3-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="332b3-116">Polecenie ustawia liczbę jednostek DTU dla puli elastycznej na 1000 oraz ustawia minimalną i maksymalną liczbę jednostek DTU.</span><span class="sxs-lookup"><span data-stu-id="332b3-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="332b3-117">Przykład 2. Modyfikowanie maksymalnego rozmiaru miejsca do magazynowania elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="332b3-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="332b3-118">To polecenie modyfikuje właściwości puli elastycznej o nazwiePoolpool01.</span><span class="sxs-lookup"><span data-stu-id="332b3-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="332b3-119">To polecenie ustawia maksymalną ilość miejsca do magazynowania elastycznego puli na 2 TB.</span><span class="sxs-lookup"><span data-stu-id="332b3-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="332b3-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="332b3-120">Example 3</span></span>

<span data-ttu-id="332b3-121">Modyfikuje właściwości elastycznej puli baz danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="332b3-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="332b3-122">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="332b3-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="332b3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="332b3-123">PARAMETERS</span></span>

### <span data-ttu-id="332b3-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="332b3-124">-AsJob</span></span>
<span data-ttu-id="332b3-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="332b3-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="332b3-126">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="332b3-126">-ComputeGeneration</span></span>
<span data-ttu-id="332b3-127">Generowanie obliczeniowe do przypisania.</span><span class="sxs-lookup"><span data-stu-id="332b3-127">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332b3-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="332b3-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="332b3-129">Określa maksymalną liczbę jednostek DTU, z których może korzystać każda pojedyncza baza danych w puli.</span><span class="sxs-lookup"><span data-stu-id="332b3-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="332b3-130">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="332b3-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="332b3-131">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="332b3-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="332b3-132">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="332b3-132">Basic.</span></span>  <span data-ttu-id="332b3-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-133">5 DTUs</span></span>
- <span data-ttu-id="332b3-134">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="332b3-134">Standard.</span></span> <span data-ttu-id="332b3-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-135">100 DTUs</span></span>
- <span data-ttu-id="332b3-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="332b3-136">Premium.</span></span> <span data-ttu-id="332b3-137">125 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-137">125 DTUs</span></span>

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

### <span data-ttu-id="332b3-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="332b3-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="332b3-139">Określa minimalną liczbę jednostek DTU, które elastyczna pula gwarantuje wszystkim bazom danych w puli.</span><span class="sxs-lookup"><span data-stu-id="332b3-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="332b3-140">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="332b3-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="332b3-141">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="332b3-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="332b3-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="332b3-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="332b3-143">Maksymalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="332b3-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="332b3-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="332b3-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="332b3-145">Minimalna liczba punktów VCore, z których każda baza danych SqlAzure może korzystać w puli.</span><span class="sxs-lookup"><span data-stu-id="332b3-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="332b3-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332b3-146">-DefaultProfile</span></span>
<span data-ttu-id="332b3-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="332b3-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="332b3-148">- Dtu</span><span class="sxs-lookup"><span data-stu-id="332b3-148">-Dtu</span></span>
<span data-ttu-id="332b3-149">Określa całkowitą liczbę współużytkonych jednostek DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="332b3-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="332b3-150">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę dla konkretnej puli rozmiarów w pulach [elastycznych.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="332b3-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="332b3-151">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="332b3-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="332b3-152">Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="332b3-152">Basic.</span></span> <span data-ttu-id="332b3-153">100 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-153">100 DTUs</span></span>
- <span data-ttu-id="332b3-154">Standardowe.</span><span class="sxs-lookup"><span data-stu-id="332b3-154">Standard.</span></span> <span data-ttu-id="332b3-155">100 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-155">100 DTUs</span></span>
- <span data-ttu-id="332b3-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="332b3-156">Premium.</span></span> <span data-ttu-id="332b3-157">125 DTU</span><span class="sxs-lookup"><span data-stu-id="332b3-157">125 DTUs</span></span>

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

### <span data-ttu-id="332b3-158">— wersja</span><span class="sxs-lookup"><span data-stu-id="332b3-158">-Edition</span></span>
<span data-ttu-id="332b3-159">Określa wersję bazy danych Azure SQL Database dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="332b3-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="332b3-160">Nie można zmienić wersji.</span><span class="sxs-lookup"><span data-stu-id="332b3-160">You cannot change the edition.</span></span> <span data-ttu-id="332b3-161">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="332b3-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="332b3-162">Brak</span><span class="sxs-lookup"><span data-stu-id="332b3-162">None</span></span>
- <span data-ttu-id="332b3-163">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="332b3-163">Basic</span></span>
- <span data-ttu-id="332b3-164">Standardowe</span><span class="sxs-lookup"><span data-stu-id="332b3-164">Standard</span></span>
- <span data-ttu-id="332b3-165">Premium</span><span class="sxs-lookup"><span data-stu-id="332b3-165">Premium</span></span>
- <span data-ttu-id="332b3-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="332b3-166">DataWarehouse</span></span>
- <span data-ttu-id="332b3-167">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="332b3-167">Free</span></span>
- <span data-ttu-id="332b3-168">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="332b3-168">Stretch</span></span>
- <span data-ttu-id="332b3-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="332b3-169">GeneralPurpose</span></span>
- <span data-ttu-id="332b3-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="332b3-170">BusinessCritical</span></span>

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

### <span data-ttu-id="332b3-171">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="332b3-171">-ElasticPoolName</span></span>
<span data-ttu-id="332b3-172">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="332b3-172">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="332b3-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="332b3-173">-LicenseType</span></span>
<span data-ttu-id="332b3-174">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="332b3-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="332b3-175">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="332b3-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="332b3-176">Identyfikator konfiguracji konserwacji puli elastycznej SQL.</span><span class="sxs-lookup"><span data-stu-id="332b3-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="332b3-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="332b3-177">-ResourceGroupName</span></span>
<span data-ttu-id="332b3-178">Określa nazwę grupy zasobów, do której jest przypisana pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="332b3-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="332b3-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="332b3-179">-ServerName</span></span>
<span data-ttu-id="332b3-180">Określa nazwę serwera hostowego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="332b3-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="332b3-181">— StorageMB</span><span class="sxs-lookup"><span data-stu-id="332b3-181">-StorageMB</span></span>
<span data-ttu-id="332b3-182">Określa limit magazynowania puli elastycznej (w megabajtach).</span><span class="sxs-lookup"><span data-stu-id="332b3-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="332b3-183">Aby uzyskać więcej informacji, zobacz New-AzSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="332b3-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="332b3-184">— Tagi</span><span class="sxs-lookup"><span data-stu-id="332b3-184">-Tags</span></span>
<span data-ttu-id="332b3-185">Określa słownik par klucz-wartość, który to polecenie cmdlet skojarzy z elastyczną pulą w postaci tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="332b3-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="332b3-186">Na przykład: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="332b3-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="332b3-187">— VCore</span><span class="sxs-lookup"><span data-stu-id="332b3-187">-VCore</span></span>
<span data-ttu-id="332b3-188">Całkowita udostępniona liczba procesorów Vcore dla puli sql Azure 2010 r.</span><span class="sxs-lookup"><span data-stu-id="332b3-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332b3-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="332b3-189">-ZoneRedundant</span></span>
<span data-ttu-id="332b3-190">Nadmiarowość stref, która ma być skojarzana z pulą Azure Sql 2010</span><span class="sxs-lookup"><span data-stu-id="332b3-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="332b3-191">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="332b3-191">-Confirm</span></span>
<span data-ttu-id="332b3-192">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="332b3-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="332b3-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="332b3-193">-WhatIf</span></span>
<span data-ttu-id="332b3-194">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="332b3-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="332b3-195">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="332b3-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="332b3-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332b3-196">CommonParameters</span></span>
<span data-ttu-id="332b3-197">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="332b3-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332b3-198">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="332b3-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332b3-199">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="332b3-199">INPUTS</span></span>

### <span data-ttu-id="332b3-200">System.String</span><span class="sxs-lookup"><span data-stu-id="332b3-200">System.String</span></span>

## <span data-ttu-id="332b3-201">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="332b3-201">OUTPUTS</span></span>

### <span data-ttu-id="332b3-202">Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="332b3-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="332b3-203">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="332b3-203">NOTES</span></span>

## <span data-ttu-id="332b3-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="332b3-204">RELATED LINKS</span></span>

[<span data-ttu-id="332b3-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="332b3-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="332b3-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="332b3-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="332b3-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="332b3-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="332b3-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="332b3-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="332b3-209">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="332b3-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
