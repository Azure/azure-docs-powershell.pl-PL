---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547896"
---
# <span data-ttu-id="e439b-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e439b-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="e439b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e439b-102">SYNOPSIS</span></span>
<span data-ttu-id="e439b-103">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e439b-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e439b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e439b-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e439b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e439b-105">DESCRIPTION</span></span>
<span data-ttu-id="e439b-106">Polecenie cmdlet **New-AzureRmSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e439b-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="e439b-107">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="e439b-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="e439b-108">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="e439b-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="e439b-109">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="e439b-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="e439b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e439b-110">EXAMPLES</span></span>

### <span data-ttu-id="e439b-111">Przykład 1. Tworzenie puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="e439b-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="e439b-112">To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="e439b-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="e439b-113">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="e439b-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="e439b-114">Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="e439b-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="e439b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e439b-115">PARAMETERS</span></span>

### <span data-ttu-id="e439b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e439b-116">-AsJob</span></span>
<span data-ttu-id="e439b-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e439b-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="e439b-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="e439b-119">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="e439b-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="e439b-120">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="e439b-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="e439b-121">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="e439b-121">Basic.</span></span> <span data-ttu-id="e439b-122">5 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-122">5 DTUs</span></span>
- <span data-ttu-id="e439b-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="e439b-123">Standard.</span></span> <span data-ttu-id="e439b-124">100 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-124">100 DTUs</span></span>
- <span data-ttu-id="e439b-125">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="e439b-125">Premium.</span></span> <span data-ttu-id="e439b-126">125 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-126">125 DTUs</span></span>

<span data-ttu-id="e439b-127">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli rozmiarów w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="e439b-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="e439b-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="e439b-129">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="e439b-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="e439b-130">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="e439b-130">The default value is zero (0).</span></span>

<span data-ttu-id="e439b-131">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="e439b-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e439b-132">-DefaultProfile</span></span>
<span data-ttu-id="e439b-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e439b-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-134">-Dtu</span></span>
<span data-ttu-id="e439b-135">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="e439b-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="e439b-136">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="e439b-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="e439b-137">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="e439b-137">Basic.</span></span>
<span data-ttu-id="e439b-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-138">100 DTUs</span></span>
- <span data-ttu-id="e439b-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="e439b-139">Standard.</span></span>
<span data-ttu-id="e439b-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-140">100 DTUs</span></span>
- <span data-ttu-id="e439b-141">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="e439b-141">Premium.</span></span>
<span data-ttu-id="e439b-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="e439b-142">125 DTUs</span></span>

<span data-ttu-id="e439b-143">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="e439b-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="e439b-144">-Edition</span></span>
<span data-ttu-id="e439b-145">Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="e439b-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="e439b-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e439b-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e439b-147">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="e439b-147">Premium</span></span>
- <span data-ttu-id="e439b-148">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="e439b-148">Basic</span></span>
- <span data-ttu-id="e439b-149">Standard</span><span class="sxs-lookup"><span data-stu-id="e439b-149">Standard</span></span>
- <span data-ttu-id="e439b-150">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="e439b-150">DataWarehouse</span></span>
- <span data-ttu-id="e439b-151">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="e439b-151">Stretch</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e439b-152">-ElasticPoolName</span></span>
<span data-ttu-id="e439b-153">Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e439b-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e439b-154">-ResourceGroupName</span></span>
<span data-ttu-id="e439b-155">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="e439b-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-156">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e439b-156">-ServerName</span></span>
<span data-ttu-id="e439b-157">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="e439b-157">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="e439b-158">-StorageMB</span></span>
<span data-ttu-id="e439b-159">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="e439b-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="e439b-160">Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .</span><span class="sxs-lookup"><span data-stu-id="e439b-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="e439b-161">Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="e439b-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-162">-Tagi</span><span class="sxs-lookup"><span data-stu-id="e439b-162">-Tags</span></span>
<span data-ttu-id="e439b-163">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną.</span><span class="sxs-lookup"><span data-stu-id="e439b-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="e439b-164">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e439b-164">For example:</span></span>

<span data-ttu-id="e439b-165">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e439b-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e439b-166">-ZoneRedundant</span></span>
<span data-ttu-id="e439b-167">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e439b-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e439b-168">-Confirm</span></span>
<span data-ttu-id="e439b-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e439b-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e439b-170">-WhatIf</span></span>
<span data-ttu-id="e439b-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e439b-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e439b-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e439b-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e439b-173">CommonParameters</span></span>
<span data-ttu-id="e439b-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e439b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e439b-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e439b-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e439b-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e439b-176">INPUTS</span></span>

### <span data-ttu-id="e439b-177">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e439b-177">None</span></span>
<span data-ttu-id="e439b-178">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e439b-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e439b-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e439b-179">OUTPUTS</span></span>

### <span data-ttu-id="e439b-180">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="e439b-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="e439b-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e439b-181">NOTES</span></span>

## <span data-ttu-id="e439b-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e439b-182">RELATED LINKS</span></span>

[<span data-ttu-id="e439b-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e439b-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e439b-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e439b-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="e439b-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="e439b-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="e439b-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e439b-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e439b-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e439b-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e439b-188">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e439b-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
