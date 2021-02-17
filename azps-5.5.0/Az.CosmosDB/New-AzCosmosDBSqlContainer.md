---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 7b773bd51a928c21761900cf1f6f8c34e73c2d0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177243"
---
# <span data-ttu-id="25328-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="25328-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="25328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25328-102">SYNOPSIS</span></span>
<span data-ttu-id="25328-103">Tworzy nowy kontener sql Dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="25328-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="25328-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25328-104">SYNTAX</span></span>

### <span data-ttu-id="25328-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="25328-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25328-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25328-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25328-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="25328-107">DESCRIPTION</span></span>
<span data-ttu-id="25328-108">Tworzy nowy kontener sql Dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="25328-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="25328-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25328-109">EXAMPLES</span></span>

### <span data-ttu-id="25328-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25328-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="25328-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25328-111">PARAMETERS</span></span>

### <span data-ttu-id="25328-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25328-112">-AccountName</span></span>
<span data-ttu-id="25328-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="25328-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="25328-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="25328-115">TTL for Analytical Storage (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="25328-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="25328-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="25328-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="25328-117">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="25328-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="25328-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25328-118">-Confirm</span></span>
<span data-ttu-id="25328-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25328-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="25328-121">Obiekt ConflictResolutionPolicy typu PSSqlConflictResolutionPolicy, jeśli jest ustawiony jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="25328-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25328-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="25328-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="25328-123">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="25328-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="25328-124">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="25328-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="25328-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="25328-126">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="25328-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="25328-127">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="25328-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="25328-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="25328-129">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="25328-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="25328-130">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="25328-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25328-131">-DatabaseName</span></span>
<span data-ttu-id="25328-132">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="25328-132">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25328-133">-DefaultProfile</span></span>
<span data-ttu-id="25328-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25328-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-135">-IndexingPolicy</span></span>
<span data-ttu-id="25328-136">Obiekt zasad indeksowania typu Microsoft.Azure.Commands.Dosdb.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="25328-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25328-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25328-137">-Name</span></span>
<span data-ttu-id="25328-138">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="25328-138">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-139">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="25328-139">-ParentObject</span></span>
<span data-ttu-id="25328-140">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="25328-140">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25328-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="25328-141">-PartitionKeyKind</span></span>
<span data-ttu-id="25328-142">Rodzaj algorytmu używanego do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="25328-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="25328-143">Możliwe wartości: "Skrót", "Zakres"</span><span class="sxs-lookup"><span data-stu-id="25328-143">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="25328-144">-PartitionKeyPath</span></span>
<span data-ttu-id="25328-145">Ścieżka klucza partycji, na przykład "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="25328-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="25328-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="25328-147">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="25328-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="25328-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25328-148">-ResourceGroupName</span></span>
<span data-ttu-id="25328-149">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25328-149">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-150">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="25328-150">-Throughput</span></span>
<span data-ttu-id="25328-151">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="25328-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="25328-152">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="25328-152">Default value is 400.</span></span>

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

### <span data-ttu-id="25328-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="25328-153">-TtlInSeconds</span></span>
<span data-ttu-id="25328-154">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="25328-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="25328-155">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="25328-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="25328-156">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="25328-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="25328-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="25328-158">Obiekt UniqueKeyPolicy typu Microsoft.Azure.Commands.Dosdb.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="25328-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25328-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25328-159">-WhatIf</span></span>
<span data-ttu-id="25328-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25328-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25328-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25328-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25328-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25328-162">CommonParameters</span></span>
<span data-ttu-id="25328-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25328-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25328-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25328-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25328-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25328-165">INPUTS</span></span>

### <span data-ttu-id="25328-166">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="25328-167">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="25328-168">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="25328-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="25328-169">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="25328-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="25328-170">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25328-170">OUTPUTS</span></span>

### <span data-ttu-id="25328-171">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="25328-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="25328-172">Microsoft.Azure.Commands.Dosdb.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="25328-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="25328-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25328-173">NOTES</span></span>

## <span data-ttu-id="25328-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25328-174">RELATED LINKS</span></span>
