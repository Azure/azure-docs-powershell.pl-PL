---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 6b059905cdc1e9474ce455f78fac88f282b5ce10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546379"
---
# <span data-ttu-id="58778-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="58778-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="58778-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58778-102">SYNOPSIS</span></span>
<span data-ttu-id="58778-103">Modyfikuje właściwości puli Elastic Database w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="58778-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58778-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58778-104">SYNTAX</span></span>

### <span data-ttu-id="58778-105">DtuBasedPool (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58778-105">DtuBasedPool (Default)</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58778-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="58778-106">VcoreBasedPool</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58778-107">Opis</span><span class="sxs-lookup"><span data-stu-id="58778-107">DESCRIPTION</span></span>
<span data-ttu-id="58778-108">Polecenie cmdlet **Set-AzureRmSqlElasticPool** ustawia właściwości puli elastycznej w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="58778-108">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="58778-109">To polecenie cmdlet może modyfikować eDTUs na pulę ( *jednostek DTU* ), maksymalny rozmiar magazynu na pulę ( *StorageMB* ), maksymalną eDTUs na bazę danych ( *DatabaseDtuMax* ) i minimalną eDTUs na bazę danych ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="58778-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="58778-110">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="58778-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="58778-111">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="58778-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="58778-112">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="58778-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="58778-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58778-113">EXAMPLES</span></span>

### <span data-ttu-id="58778-114">Przykład 1. Modyfikowanie właściwości elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="58778-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="58778-115">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="58778-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="58778-116">To polecenie ustawia liczbę DTU dla puli elastycznej na 1000 i ustawia minimalną i maksymalną Dtuę.</span><span class="sxs-lookup"><span data-stu-id="58778-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="58778-117">Przykład 2: modyfikowanie maksymalnego rozmiaru magazynu elastycznego</span><span class="sxs-lookup"><span data-stu-id="58778-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="58778-118">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="58778-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="58778-119">Polecenie ustawia maksymalną ilość miejsca do magazynowania dla elastycznego zestawu na 2 TB.</span><span class="sxs-lookup"><span data-stu-id="58778-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="58778-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58778-120">PARAMETERS</span></span>

### <span data-ttu-id="58778-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58778-121">-AsJob</span></span>
<span data-ttu-id="58778-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="58778-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58778-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="58778-123">-ComputeGeneration</span></span>
<span data-ttu-id="58778-124">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="58778-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="58778-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="58778-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="58778-126">Określa maksymalną liczbę DTU, które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="58778-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="58778-127">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="58778-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="58778-128">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="58778-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="58778-129">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="58778-129">Basic.</span></span>  <span data-ttu-id="58778-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-130">5 DTUs</span></span>
- <span data-ttu-id="58778-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="58778-131">Standard.</span></span> <span data-ttu-id="58778-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-132">100 DTUs</span></span>
- <span data-ttu-id="58778-133">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="58778-133">Premium.</span></span> <span data-ttu-id="58778-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-134">125 DTUs</span></span>

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

### <span data-ttu-id="58778-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="58778-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="58778-136">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="58778-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="58778-137">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="58778-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="58778-138">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="58778-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="58778-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="58778-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="58778-140">Numer VCore Maxmium, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="58778-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="58778-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="58778-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="58778-142">Minimalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="58778-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="58778-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58778-143">-DefaultProfile</span></span>
<span data-ttu-id="58778-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="58778-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58778-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="58778-145">-Dtu</span></span>
<span data-ttu-id="58778-146">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="58778-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="58778-147">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="58778-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="58778-148">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="58778-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="58778-149">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="58778-149">Basic.</span></span> <span data-ttu-id="58778-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-150">100 DTUs</span></span>
- <span data-ttu-id="58778-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="58778-151">Standard.</span></span> <span data-ttu-id="58778-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-152">100 DTUs</span></span>
- <span data-ttu-id="58778-153">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="58778-153">Premium.</span></span> <span data-ttu-id="58778-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="58778-154">125 DTUs</span></span>

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

### <span data-ttu-id="58778-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="58778-155">-Edition</span></span>
<span data-ttu-id="58778-156">Określa wersję bazy danych SQL Azure dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="58778-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="58778-157">Nie można zmienić tej wersji.</span><span class="sxs-lookup"><span data-stu-id="58778-157">You cannot change the edition.</span></span> <span data-ttu-id="58778-158">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58778-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58778-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58778-159">None</span></span>
- <span data-ttu-id="58778-160">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="58778-160">Basic</span></span>
- <span data-ttu-id="58778-161">Standard</span><span class="sxs-lookup"><span data-stu-id="58778-161">Standard</span></span>
- <span data-ttu-id="58778-162">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="58778-162">Premium</span></span>
- <span data-ttu-id="58778-163">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="58778-163">DataWarehouse</span></span>
- <span data-ttu-id="58778-164">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="58778-164">Free</span></span>
- <span data-ttu-id="58778-165">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="58778-165">Stretch</span></span>
- <span data-ttu-id="58778-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="58778-166">GeneralPurpose</span></span>
- <span data-ttu-id="58778-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="58778-167">BusinessCritical</span></span>

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

### <span data-ttu-id="58778-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="58778-168">-ElasticPoolName</span></span>
<span data-ttu-id="58778-169">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="58778-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="58778-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="58778-170">-LicenseType</span></span>
<span data-ttu-id="58778-171">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="58778-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="58778-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58778-172">-ResourceGroupName</span></span>
<span data-ttu-id="58778-173">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="58778-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="58778-174">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="58778-174">-ServerName</span></span>
<span data-ttu-id="58778-175">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="58778-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="58778-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="58778-176">-StorageMB</span></span>
<span data-ttu-id="58778-177">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="58778-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="58778-178">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="58778-178">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="58778-179">-Tagi</span><span class="sxs-lookup"><span data-stu-id="58778-179">-Tags</span></span>
<span data-ttu-id="58778-180">Określa słownik par klucz-wartość, które to polecenie cmdlet kojarzy z pulą elastyczną w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="58778-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="58778-181">Na przykład: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="58778-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="58778-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="58778-182">-VCore</span></span>
<span data-ttu-id="58778-183">Łączna przydzielona liczba vCore dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="58778-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="58778-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="58778-184">-ZoneRedundant</span></span>
<span data-ttu-id="58778-185">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="58778-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="58778-186">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58778-186">-Confirm</span></span>
<span data-ttu-id="58778-187">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58778-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58778-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58778-188">-WhatIf</span></span>
<span data-ttu-id="58778-189">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58778-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58778-190">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58778-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58778-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58778-191">CommonParameters</span></span>
<span data-ttu-id="58778-192">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58778-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58778-193">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58778-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58778-194">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58778-194">INPUTS</span></span>

### <span data-ttu-id="58778-195">System. String</span><span class="sxs-lookup"><span data-stu-id="58778-195">System.String</span></span>

## <span data-ttu-id="58778-196">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58778-196">OUTPUTS</span></span>

### <span data-ttu-id="58778-197">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="58778-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="58778-198">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58778-198">NOTES</span></span>

## <span data-ttu-id="58778-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58778-199">RELATED LINKS</span></span>

[<span data-ttu-id="58778-200">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="58778-200">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="58778-201">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="58778-201">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="58778-202">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="58778-202">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="58778-203">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="58778-203">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="58778-204">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="58778-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
