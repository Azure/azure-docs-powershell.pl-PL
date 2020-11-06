---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542807"
---
# <span data-ttu-id="9294f-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9294f-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="9294f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9294f-102">SYNOPSIS</span></span>
<span data-ttu-id="9294f-103">Modyfikuje właściwości puli Elastic Database w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9294f-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9294f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9294f-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9294f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9294f-105">DESCRIPTION</span></span>
<span data-ttu-id="9294f-106">Polecenie cmdlet **Set-AzureRmSqlElasticPool** modyfikuje właściwości elastycznego zestawu baz danych w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9294f-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="9294f-107">To polecenie cmdlet może zmodyfikować minimalne jednostki produktywności bazy danych (DTU) na bazę danych oprócz maksymalnej DTU na bazę danych, liczbę DTU dla puli oraz limit magazynowania dla puli.</span><span class="sxs-lookup"><span data-stu-id="9294f-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="9294f-108">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="9294f-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="9294f-109">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="9294f-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="9294f-110">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9294f-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="9294f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9294f-111">EXAMPLES</span></span>

### <span data-ttu-id="9294f-112">Przykład 1. Modyfikowanie właściwości elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="9294f-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="9294f-113">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="9294f-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="9294f-114">To polecenie ustawia liczbę DTU dla puli elastycznej na 1000 i ustawia minimalną i maksymalną Dtuę.</span><span class="sxs-lookup"><span data-stu-id="9294f-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="9294f-115">Przykład 2: modyfikowanie maksymalnej ilości miejsca do magazynowania dla puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="9294f-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="9294f-116">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="9294f-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="9294f-117">Polecenie ustawia maksymalną ilość miejsca do magazynowania dla elastycznego zestawu na 2 TB.</span><span class="sxs-lookup"><span data-stu-id="9294f-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="9294f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9294f-118">PARAMETERS</span></span>

### <span data-ttu-id="9294f-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="9294f-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="9294f-120">Określa maksymalną liczbę DTU, które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="9294f-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="9294f-121">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9294f-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="9294f-122">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="9294f-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="9294f-123">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="9294f-123">Basic.</span></span>  <span data-ttu-id="9294f-124">5 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-124">5 DTUs</span></span>
- <span data-ttu-id="9294f-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="9294f-125">Standard.</span></span> <span data-ttu-id="9294f-126">100 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-126">100 DTUs</span></span>
- <span data-ttu-id="9294f-127">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="9294f-127">Premium.</span></span> <span data-ttu-id="9294f-128">125 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-128">125 DTUs</span></span>


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

### <span data-ttu-id="9294f-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="9294f-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="9294f-130">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="9294f-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="9294f-131">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9294f-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="9294f-132">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="9294f-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="9294f-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-133">-Dtu</span></span>
<span data-ttu-id="9294f-134">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="9294f-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="9294f-135">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9294f-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="9294f-136">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="9294f-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="9294f-137">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="9294f-137">Basic.</span></span> <span data-ttu-id="9294f-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-138">100 DTUs</span></span>
- <span data-ttu-id="9294f-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="9294f-139">Standard.</span></span> <span data-ttu-id="9294f-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-140">100 DTUs</span></span>
- <span data-ttu-id="9294f-141">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="9294f-141">Premium.</span></span> <span data-ttu-id="9294f-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="9294f-142">125 DTUs</span></span>

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

### <span data-ttu-id="9294f-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="9294f-143">-Edition</span></span>
<span data-ttu-id="9294f-144">Określa wersję bazy danych SQL Azure dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="9294f-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="9294f-145">Nie można zmienić tej wersji.</span><span class="sxs-lookup"><span data-stu-id="9294f-145">You cannot change the edition.</span></span> <span data-ttu-id="9294f-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9294f-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9294f-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9294f-147">None</span></span>
- <span data-ttu-id="9294f-148">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="9294f-148">Basic</span></span>
- <span data-ttu-id="9294f-149">Standard</span><span class="sxs-lookup"><span data-stu-id="9294f-149">Standard</span></span>
- <span data-ttu-id="9294f-150">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="9294f-150">Premium</span></span>
- <span data-ttu-id="9294f-151">Składki</span><span class="sxs-lookup"><span data-stu-id="9294f-151">PremiumRS</span></span>
- <span data-ttu-id="9294f-152">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="9294f-152">DataWarehouse</span></span>
- <span data-ttu-id="9294f-153">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="9294f-153">Free</span></span>

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

### <span data-ttu-id="9294f-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9294f-154">-ElasticPoolName</span></span>
<span data-ttu-id="9294f-155">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="9294f-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="9294f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9294f-156">-ResourceGroupName</span></span>
<span data-ttu-id="9294f-157">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="9294f-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="9294f-158">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9294f-158">-ServerName</span></span>
<span data-ttu-id="9294f-159">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="9294f-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="9294f-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="9294f-160">-StorageMB</span></span>
<span data-ttu-id="9294f-161">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="9294f-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="9294f-162">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="9294f-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="9294f-163">-Tagi</span><span class="sxs-lookup"><span data-stu-id="9294f-163">-Tags</span></span>
<span data-ttu-id="9294f-164">Określa słownik par klucz-wartość, które to polecenie cmdlet kojarzy z pulą elastyczną w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9294f-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="9294f-165">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="9294f-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="9294f-166">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9294f-166">-Confirm</span></span>
<span data-ttu-id="9294f-167">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9294f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9294f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9294f-168">-WhatIf</span></span>
<span data-ttu-id="9294f-169">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9294f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9294f-170">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9294f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9294f-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9294f-171">-DefaultProfile</span></span>
<span data-ttu-id="9294f-172">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9294f-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9294f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9294f-173">CommonParameters</span></span>
<span data-ttu-id="9294f-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9294f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9294f-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9294f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9294f-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9294f-176">INPUTS</span></span>

## <span data-ttu-id="9294f-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9294f-177">OUTPUTS</span></span>

### <span data-ttu-id="9294f-178">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="9294f-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="9294f-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9294f-179">NOTES</span></span>

## <span data-ttu-id="9294f-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9294f-180">RELATED LINKS</span></span>

[<span data-ttu-id="9294f-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9294f-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="9294f-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9294f-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="9294f-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="9294f-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="9294f-184">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9294f-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="9294f-185">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="9294f-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
