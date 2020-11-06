---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547856"
---
# <span data-ttu-id="97d26-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="97d26-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="97d26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97d26-102">SYNOPSIS</span></span>
<span data-ttu-id="97d26-103">Modyfikuje właściwości puli Elastic Database w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="97d26-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97d26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97d26-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97d26-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97d26-105">DESCRIPTION</span></span>
<span data-ttu-id="97d26-106">Polecenie cmdlet **Set-AzureRmSqlElasticPool** ustawia właściwości puli elastycznej w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="97d26-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="97d26-107">To polecenie cmdlet może modyfikować eDTUs na pulę ( *jednostek DTU* ), maksymalny rozmiar magazynu na pulę ( *StorageMB* ), maksymalną eDTUs na bazę danych ( *DatabaseDtuMax* ) i minimalną eDTUs na bazę danych ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="97d26-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="97d26-108">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="97d26-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="97d26-109">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="97d26-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="97d26-110">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="97d26-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="97d26-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97d26-111">EXAMPLES</span></span>

### <span data-ttu-id="97d26-112">Przykład 1. Modyfikowanie właściwości elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="97d26-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="97d26-113">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="97d26-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="97d26-114">To polecenie ustawia liczbę DTU dla puli elastycznej na 1000 i ustawia minimalną i maksymalną Dtuę.</span><span class="sxs-lookup"><span data-stu-id="97d26-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="97d26-115">Przykład 2: modyfikowanie maksymalnego rozmiaru magazynu elastycznego</span><span class="sxs-lookup"><span data-stu-id="97d26-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="97d26-116">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="97d26-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="97d26-117">Polecenie ustawia maksymalną ilość miejsca do magazynowania dla elastycznego zestawu na 2 TB.</span><span class="sxs-lookup"><span data-stu-id="97d26-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="97d26-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97d26-118">PARAMETERS</span></span>

### <span data-ttu-id="97d26-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97d26-119">-AsJob</span></span>
<span data-ttu-id="97d26-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="97d26-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="97d26-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="97d26-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="97d26-122">Określa maksymalną liczbę DTU, które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="97d26-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="97d26-123">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="97d26-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="97d26-124">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="97d26-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="97d26-125">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="97d26-125">Basic.</span></span>  <span data-ttu-id="97d26-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-126">5 DTUs</span></span>
- <span data-ttu-id="97d26-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="97d26-127">Standard.</span></span> <span data-ttu-id="97d26-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-128">100 DTUs</span></span>
- <span data-ttu-id="97d26-129">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="97d26-129">Premium.</span></span> <span data-ttu-id="97d26-130">125 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-130">125 DTUs</span></span>


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

### <span data-ttu-id="97d26-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="97d26-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="97d26-132">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="97d26-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="97d26-133">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="97d26-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="97d26-134">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="97d26-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="97d26-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d26-135">-DefaultProfile</span></span>
<span data-ttu-id="97d26-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97d26-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97d26-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-137">-Dtu</span></span>
<span data-ttu-id="97d26-138">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="97d26-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="97d26-139">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="97d26-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="97d26-140">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="97d26-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="97d26-141">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="97d26-141">Basic.</span></span> <span data-ttu-id="97d26-142">100 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-142">100 DTUs</span></span>
- <span data-ttu-id="97d26-143">Standard.</span><span class="sxs-lookup"><span data-stu-id="97d26-143">Standard.</span></span> <span data-ttu-id="97d26-144">100 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-144">100 DTUs</span></span>
- <span data-ttu-id="97d26-145">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="97d26-145">Premium.</span></span> <span data-ttu-id="97d26-146">125 DTU</span><span class="sxs-lookup"><span data-stu-id="97d26-146">125 DTUs</span></span>

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

### <span data-ttu-id="97d26-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="97d26-147">-Edition</span></span>
<span data-ttu-id="97d26-148">Określa wersję bazy danych SQL Azure dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="97d26-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="97d26-149">Nie można zmienić tej wersji.</span><span class="sxs-lookup"><span data-stu-id="97d26-149">You cannot change the edition.</span></span> <span data-ttu-id="97d26-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="97d26-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97d26-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97d26-151">None</span></span>
- <span data-ttu-id="97d26-152">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="97d26-152">Basic</span></span>
- <span data-ttu-id="97d26-153">Standard</span><span class="sxs-lookup"><span data-stu-id="97d26-153">Standard</span></span>
- <span data-ttu-id="97d26-154">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="97d26-154">Premium</span></span>
- <span data-ttu-id="97d26-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="97d26-155">DataWarehouse</span></span>

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

### <span data-ttu-id="97d26-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="97d26-156">-ElasticPoolName</span></span>
<span data-ttu-id="97d26-157">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="97d26-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d26-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d26-158">-ResourceGroupName</span></span>
<span data-ttu-id="97d26-159">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="97d26-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="97d26-160">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="97d26-160">-ServerName</span></span>
<span data-ttu-id="97d26-161">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="97d26-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="97d26-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="97d26-162">-StorageMB</span></span>
<span data-ttu-id="97d26-163">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="97d26-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="97d26-164">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="97d26-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="97d26-165">-Tagi</span><span class="sxs-lookup"><span data-stu-id="97d26-165">-Tags</span></span>
<span data-ttu-id="97d26-166">Określa słownik par klucz-wartość, które to polecenie cmdlet kojarzy z pulą elastyczną w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="97d26-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="97d26-167">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="97d26-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="97d26-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="97d26-168">-ZoneRedundant</span></span>
<span data-ttu-id="97d26-169">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="97d26-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="97d26-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97d26-170">-Confirm</span></span>
<span data-ttu-id="97d26-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97d26-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d26-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d26-172">-WhatIf</span></span>
<span data-ttu-id="97d26-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97d26-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97d26-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97d26-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d26-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d26-175">CommonParameters</span></span>
<span data-ttu-id="97d26-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97d26-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d26-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97d26-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d26-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97d26-178">INPUTS</span></span>

### <span data-ttu-id="97d26-179">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97d26-179">None</span></span>
<span data-ttu-id="97d26-180">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="97d26-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97d26-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97d26-181">OUTPUTS</span></span>

### <span data-ttu-id="97d26-182">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="97d26-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="97d26-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97d26-183">NOTES</span></span>

## <span data-ttu-id="97d26-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97d26-184">RELATED LINKS</span></span>

[<span data-ttu-id="97d26-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="97d26-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="97d26-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="97d26-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="97d26-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="97d26-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="97d26-188">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="97d26-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="97d26-189">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="97d26-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
