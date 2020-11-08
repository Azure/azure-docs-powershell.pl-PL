---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222842"
---
# <span data-ttu-id="0e67e-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0e67e-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="0e67e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e67e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e67e-103">Modyfikuje właściwości puli Elastic Database w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0e67e-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="0e67e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e67e-104">SYNTAX</span></span>

### <span data-ttu-id="0e67e-105">DtuBasedPool (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e67e-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e67e-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0e67e-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e67e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e67e-107">DESCRIPTION</span></span>
<span data-ttu-id="0e67e-108">Polecenie cmdlet **Set-AzSqlElasticPool** ustawia właściwości puli elastycznej w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0e67e-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="0e67e-109">To polecenie cmdlet może modyfikować eDTUs na pulę ( *jednostek DTU* ), maksymalny rozmiar magazynu na pulę ( *StorageMB* ), maksymalną eDTUs na bazę danych ( *DatabaseDtuMax* ) i minimalną eDTUs na bazę danych ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="0e67e-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="0e67e-110">Kilka parametrów ( *-DTU,-DatabaseDtuMin i-DatabaseDtuMax* ) wymaga ustawienia wartości z listy prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="0e67e-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0e67e-111">Na przykład — DatabaseDtuMax dla standardowej puli jednostek eDTU 100 można ustawić tylko na wartość 10, 20, 50 lub 100.</span><span class="sxs-lookup"><span data-stu-id="0e67e-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0e67e-112">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0e67e-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0e67e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e67e-113">EXAMPLES</span></span>

### <span data-ttu-id="0e67e-114">Przykład 1. Modyfikowanie właściwości elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="0e67e-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="0e67e-115">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0e67e-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0e67e-116">To polecenie ustawia liczbę DTU dla puli elastycznej na 1000 i ustawia minimalną i maksymalną Dtuę.</span><span class="sxs-lookup"><span data-stu-id="0e67e-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="0e67e-117">Przykład 2: modyfikowanie maksymalnego rozmiaru magazynu elastycznego</span><span class="sxs-lookup"><span data-stu-id="0e67e-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="0e67e-118">To polecenie modyfikuje właściwości elastycznego zestawu o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0e67e-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0e67e-119">Polecenie ustawia maksymalną ilość miejsca do magazynowania dla elastycznego zestawu na 2 TB.</span><span class="sxs-lookup"><span data-stu-id="0e67e-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="0e67e-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0e67e-120">Example 3</span></span>

<span data-ttu-id="0e67e-121">Modyfikuje właściwości puli Elastic Database w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0e67e-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="0e67e-122">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="0e67e-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="0e67e-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e67e-123">PARAMETERS</span></span>

### <span data-ttu-id="0e67e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e67e-124">-AsJob</span></span>
<span data-ttu-id="0e67e-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0e67e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e67e-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0e67e-126">-ComputeGeneration</span></span>
<span data-ttu-id="0e67e-127">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="0e67e-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="0e67e-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0e67e-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="0e67e-129">Określa maksymalną liczbę DTU, które mogą być używane przez dowolną pojedynczą bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="0e67e-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="0e67e-130">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0e67e-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0e67e-131">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="0e67e-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0e67e-132">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="0e67e-132">Basic.</span></span>  <span data-ttu-id="0e67e-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-133">5 DTUs</span></span>
- <span data-ttu-id="0e67e-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="0e67e-134">Standard.</span></span> <span data-ttu-id="0e67e-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-135">100 DTUs</span></span>
- <span data-ttu-id="0e67e-136">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="0e67e-136">Premium.</span></span> <span data-ttu-id="0e67e-137">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-137">125 DTUs</span></span>

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

### <span data-ttu-id="0e67e-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0e67e-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="0e67e-139">Określa minimalną liczbę DTU, jaką Pula elastyczna gwarantuje wszystkim bazę danych w puli.</span><span class="sxs-lookup"><span data-stu-id="0e67e-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0e67e-140">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0e67e-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0e67e-141">Wartość domyślna to zero (0).</span><span class="sxs-lookup"><span data-stu-id="0e67e-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="0e67e-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0e67e-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0e67e-143">Maksymalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="0e67e-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0e67e-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0e67e-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0e67e-145">Minimalny numer VCore, który może zużyć baza danych SqlAzure w puli.</span><span class="sxs-lookup"><span data-stu-id="0e67e-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0e67e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e67e-146">-DefaultProfile</span></span>
<span data-ttu-id="0e67e-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e67e-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e67e-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-148">-Dtu</span></span>
<span data-ttu-id="0e67e-149">Określa całkowitą liczbę udostępnionych DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="0e67e-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0e67e-150">Aby uzyskać szczegółowe informacje o tym, które wartości są prawidłowe, zobacz tabelę określonej puli wielkości w [pulach elastyczny](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0e67e-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0e67e-151">Wartości domyślne dla różnych wersji są następujące:</span><span class="sxs-lookup"><span data-stu-id="0e67e-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0e67e-152">Podstawowym.</span><span class="sxs-lookup"><span data-stu-id="0e67e-152">Basic.</span></span> <span data-ttu-id="0e67e-153">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-153">100 DTUs</span></span>
- <span data-ttu-id="0e67e-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="0e67e-154">Standard.</span></span> <span data-ttu-id="0e67e-155">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-155">100 DTUs</span></span>
- <span data-ttu-id="0e67e-156">Ubezpieczeni.</span><span class="sxs-lookup"><span data-stu-id="0e67e-156">Premium.</span></span> <span data-ttu-id="0e67e-157">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0e67e-157">125 DTUs</span></span>

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

### <span data-ttu-id="0e67e-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="0e67e-158">-Edition</span></span>
<span data-ttu-id="0e67e-159">Określa wersję bazy danych SQL Azure dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="0e67e-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="0e67e-160">Nie można zmienić tej wersji.</span><span class="sxs-lookup"><span data-stu-id="0e67e-160">You cannot change the edition.</span></span> <span data-ttu-id="0e67e-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0e67e-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e67e-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e67e-162">None</span></span>
- <span data-ttu-id="0e67e-163">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="0e67e-163">Basic</span></span>
- <span data-ttu-id="0e67e-164">Standard</span><span class="sxs-lookup"><span data-stu-id="0e67e-164">Standard</span></span>
- <span data-ttu-id="0e67e-165">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="0e67e-165">Premium</span></span>
- <span data-ttu-id="0e67e-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0e67e-166">DataWarehouse</span></span>
- <span data-ttu-id="0e67e-167">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="0e67e-167">Free</span></span>
- <span data-ttu-id="0e67e-168">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="0e67e-168">Stretch</span></span>
- <span data-ttu-id="0e67e-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0e67e-169">GeneralPurpose</span></span>
- <span data-ttu-id="0e67e-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0e67e-170">BusinessCritical</span></span>

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

### <span data-ttu-id="0e67e-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0e67e-171">-ElasticPoolName</span></span>
<span data-ttu-id="0e67e-172">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="0e67e-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="0e67e-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0e67e-173">-LicenseType</span></span>
<span data-ttu-id="0e67e-174">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0e67e-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0e67e-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e67e-175">-ResourceGroupName</span></span>
<span data-ttu-id="0e67e-176">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="0e67e-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0e67e-177">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0e67e-177">-ServerName</span></span>
<span data-ttu-id="0e67e-178">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="0e67e-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0e67e-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0e67e-179">-StorageMB</span></span>
<span data-ttu-id="0e67e-180">Określa limit magazynowania (w megabajtach) dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="0e67e-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0e67e-181">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="0e67e-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="0e67e-182">-Tagi</span><span class="sxs-lookup"><span data-stu-id="0e67e-182">-Tags</span></span>
<span data-ttu-id="0e67e-183">Określa słownik par klucz-wartość, które to polecenie cmdlet kojarzy z pulą elastyczną w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0e67e-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="0e67e-184">Na przykład: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="0e67e-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="0e67e-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="0e67e-185">-VCore</span></span>
<span data-ttu-id="0e67e-186">Łączna przydzielona liczba vCore dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0e67e-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="0e67e-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0e67e-187">-ZoneRedundant</span></span>
<span data-ttu-id="0e67e-188">Nadmiarowość strefy do skojarzenia z pulą elastyczną platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="0e67e-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0e67e-189">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e67e-189">-Confirm</span></span>
<span data-ttu-id="0e67e-190">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e67e-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e67e-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e67e-191">-WhatIf</span></span>
<span data-ttu-id="0e67e-192">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e67e-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e67e-193">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e67e-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e67e-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e67e-194">CommonParameters</span></span>
<span data-ttu-id="0e67e-195">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e67e-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e67e-196">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e67e-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e67e-197">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e67e-197">INPUTS</span></span>

### <span data-ttu-id="0e67e-198">System. String</span><span class="sxs-lookup"><span data-stu-id="0e67e-198">System.String</span></span>

## <span data-ttu-id="0e67e-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e67e-199">OUTPUTS</span></span>

### <span data-ttu-id="0e67e-200">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="0e67e-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0e67e-201">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e67e-201">NOTES</span></span>

## <span data-ttu-id="0e67e-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e67e-202">RELATED LINKS</span></span>

[<span data-ttu-id="0e67e-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0e67e-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0e67e-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0e67e-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0e67e-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0e67e-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0e67e-206">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0e67e-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0e67e-207">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0e67e-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
