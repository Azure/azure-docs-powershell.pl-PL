---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719610"
---
# <span data-ttu-id="23e28-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23e28-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="23e28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23e28-102">SYNOPSIS</span></span>
<span data-ttu-id="23e28-103">Tworzy pulę Elastic Database dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="23e28-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23e28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23e28-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23e28-105">DESCRIPTION</span></span>
<span data-ttu-id="23e28-106">Polecenie cmdlet **New-AzureRmSqlElasticPool** tworzy pulę Elastic Database dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="23e28-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="23e28-107">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="23e28-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="23e28-108">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="23e28-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="23e28-109">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="23e28-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="23e28-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23e28-110">EXAMPLES</span></span>

### <span data-ttu-id="23e28-111">Przykład 1. Tworzenie puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="23e28-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="23e28-112">To polecenie tworzy elastyczną pulę w standardowej warstwie usługi o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="23e28-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="23e28-113">Serwer o nazwie Server01, przypisany do grupy zasobów platformy Azure o nazwie ResourceGroup01, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="23e28-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="23e28-114">Polecenie określa wartości właściwości jednostek DTU dla puli i baz danych w puli.</span><span class="sxs-lookup"><span data-stu-id="23e28-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="23e28-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23e28-115">PARAMETERS</span></span>

### <span data-ttu-id="23e28-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="23e28-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="23e28-117">Określa maksymalną liczbę jednostek przepływności bazy danych (DTU), które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="23e28-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="23e28-118">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="23e28-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="23e28-119">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="23e28-119">Basic.</span></span> <span data-ttu-id="23e28-120">5 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-120">5 DTUs</span></span>
- <span data-ttu-id="23e28-121">Standard.</span><span class="sxs-lookup"><span data-stu-id="23e28-121">Standard.</span></span> <span data-ttu-id="23e28-122">100 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-122">100 DTUs</span></span>
- <span data-ttu-id="23e28-123">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="23e28-123">Premium.</span></span> <span data-ttu-id="23e28-124">125 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-124">125 DTUs</span></span>

<span data-ttu-id="23e28-125">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli rozmiarów w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="23e28-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="23e28-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="23e28-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="23e28-127">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="23e28-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="23e28-128">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="23e28-128">The default value is zero (0).</span></span>

<span data-ttu-id="23e28-129">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="23e28-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="23e28-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-130">-Dtu</span></span>
<span data-ttu-id="23e28-131">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="23e28-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="23e28-132">Domyślne wartości różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="23e28-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="23e28-133">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="23e28-133">Basic.</span></span>
<span data-ttu-id="23e28-134">100 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-134">100 DTUs</span></span>
- <span data-ttu-id="23e28-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="23e28-135">Standard.</span></span>
<span data-ttu-id="23e28-136">100 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-136">100 DTUs</span></span>
- <span data-ttu-id="23e28-137">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="23e28-137">Premium.</span></span>
<span data-ttu-id="23e28-138">125 DTU</span><span class="sxs-lookup"><span data-stu-id="23e28-138">125 DTUs</span></span>

<span data-ttu-id="23e28-139">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="23e28-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="23e28-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="23e28-140">-Edition</span></span>
<span data-ttu-id="23e28-141">Określa wersję bazy danych SQL Azure używanej dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="23e28-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="23e28-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="23e28-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23e28-143">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="23e28-143">Premium</span></span>
- <span data-ttu-id="23e28-144">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="23e28-144">Basic</span></span>
- <span data-ttu-id="23e28-145">Standard</span><span class="sxs-lookup"><span data-stu-id="23e28-145">Standard</span></span>
- <span data-ttu-id="23e28-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="23e28-146">DataWarehouse</span></span>
- <span data-ttu-id="23e28-147">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="23e28-147">Stretch</span></span>
- <span data-ttu-id="23e28-148">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="23e28-148">Free</span></span>
- <span data-ttu-id="23e28-149">Składki</span><span class="sxs-lookup"><span data-stu-id="23e28-149">PremiumRS</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e28-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="23e28-150">-ElasticPoolName</span></span>
<span data-ttu-id="23e28-151">Określa nazwę puli elastycznej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e28-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="23e28-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e28-152">-ResourceGroupName</span></span>
<span data-ttu-id="23e28-153">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="23e28-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="23e28-154">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="23e28-154">-ServerName</span></span>
<span data-ttu-id="23e28-155">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="23e28-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="23e28-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="23e28-156">-StorageMB</span></span>
<span data-ttu-id="23e28-157">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="23e28-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="23e28-158">Jeśli nie podano tego parametru, to polecenie cmdlet oblicza wartość zależną od wartości parametru *jednostek DTU* .</span><span class="sxs-lookup"><span data-stu-id="23e28-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="23e28-159">Zobacz [limity liczby jednostek eDTU i przestrzeni dyskowej,](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) Aby uzyskać dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="23e28-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="23e28-160">-Tagi</span><span class="sxs-lookup"><span data-stu-id="23e28-160">-Tags</span></span>
<span data-ttu-id="23e28-161">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z pulą elastyczną.</span><span class="sxs-lookup"><span data-stu-id="23e28-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="23e28-162">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="23e28-162">For example:</span></span>

<span data-ttu-id="23e28-163">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="23e28-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="23e28-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23e28-164">-Confirm</span></span>
<span data-ttu-id="23e28-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e28-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e28-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e28-166">-WhatIf</span></span>
<span data-ttu-id="23e28-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e28-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e28-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23e28-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e28-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e28-169">-DefaultProfile</span></span>
<span data-ttu-id="23e28-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23e28-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23e28-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e28-171">CommonParameters</span></span>
<span data-ttu-id="23e28-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e28-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e28-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e28-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e28-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23e28-174">INPUTS</span></span>

## <span data-ttu-id="23e28-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23e28-175">OUTPUTS</span></span>

### <span data-ttu-id="23e28-176">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="23e28-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="23e28-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23e28-177">NOTES</span></span>

## <span data-ttu-id="23e28-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23e28-178">RELATED LINKS</span></span>

[<span data-ttu-id="23e28-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23e28-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="23e28-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="23e28-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="23e28-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="23e28-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="23e28-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23e28-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="23e28-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23e28-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="23e28-184">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="23e28-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
