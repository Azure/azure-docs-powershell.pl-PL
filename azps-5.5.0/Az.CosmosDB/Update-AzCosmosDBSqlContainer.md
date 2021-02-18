---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 60bbe085aaaa65c65ba33839db5f02ae5198e155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181242"
---
# <span data-ttu-id="d6101-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="d6101-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="d6101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6101-102">SYNOPSIS</span></span>
<span data-ttu-id="d6101-103">Aktualizuje kontener sql dla firmy DossDB.</span><span class="sxs-lookup"><span data-stu-id="d6101-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="d6101-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący kontener.</span><span class="sxs-lookup"><span data-stu-id="d6101-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="d6101-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6101-105">SYNTAX</span></span>

### <span data-ttu-id="d6101-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6101-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6101-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6101-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6101-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6101-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6101-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6101-109">DESCRIPTION</span></span>
<span data-ttu-id="d6101-110">Aktualizuje kontener sql dla firmy DossDB.</span><span class="sxs-lookup"><span data-stu-id="d6101-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="d6101-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący kontener.</span><span class="sxs-lookup"><span data-stu-id="d6101-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="d6101-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6101-112">EXAMPLES</span></span>

### <span data-ttu-id="d6101-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6101-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="d6101-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6101-114">PARAMETERS</span></span>

### <span data-ttu-id="d6101-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6101-115">-AccountName</span></span>
<span data-ttu-id="d6101-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="d6101-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d6101-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="d6101-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="d6101-118">TTL for Analytical Storage (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="d6101-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="d6101-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d6101-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d6101-120">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="d6101-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d6101-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6101-121">-Confirm</span></span>
<span data-ttu-id="d6101-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6101-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6101-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d6101-124">Obiekt ConflictResolutionPolicy typu PSSqlConflictResolutionPolicy, jeśli jest ustawiony jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6101-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d6101-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d6101-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d6101-126">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="d6101-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="d6101-127">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="d6101-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d6101-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d6101-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d6101-129">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="d6101-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="d6101-130">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="d6101-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d6101-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d6101-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d6101-132">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="d6101-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="d6101-133">Jeśli zostanie podany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="d6101-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="d6101-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6101-134">-DatabaseName</span></span>
<span data-ttu-id="d6101-135">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d6101-135">Database name.</span></span>

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

### <span data-ttu-id="d6101-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6101-136">-DefaultProfile</span></span>
<span data-ttu-id="d6101-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6101-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6101-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-138">-IndexingPolicy</span></span>
<span data-ttu-id="d6101-139">Obiekt zasad indeksowania typu Microsoft.Azure.Commands.Dosdb.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d6101-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="d6101-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6101-140">-InputObject</span></span>
<span data-ttu-id="d6101-141">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="d6101-141">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6101-142">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6101-142">-Name</span></span>
<span data-ttu-id="d6101-143">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6101-143">Container name.</span></span>

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

### <span data-ttu-id="d6101-144">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d6101-144">-ParentObject</span></span>
<span data-ttu-id="d6101-145">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="d6101-145">Sql Database object.</span></span>

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

### <span data-ttu-id="d6101-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d6101-146">-PartitionKeyKind</span></span>
<span data-ttu-id="d6101-147">Rodzaj algorytmu używanego do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="d6101-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d6101-148">Możliwe wartości: "Skrót", "Zakres"</span><span class="sxs-lookup"><span data-stu-id="d6101-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="d6101-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d6101-149">-PartitionKeyPath</span></span>
<span data-ttu-id="d6101-150">Ścieżka klucza partycji, na przykład "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="d6101-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6101-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d6101-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="d6101-152">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="d6101-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d6101-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6101-153">-ResourceGroupName</span></span>
<span data-ttu-id="d6101-154">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6101-154">Name of resource group.</span></span>

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

### <span data-ttu-id="d6101-155">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="d6101-155">-Throughput</span></span>
<span data-ttu-id="d6101-156">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d6101-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="d6101-157">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="d6101-157">Default value is 400.</span></span>

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

### <span data-ttu-id="d6101-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d6101-158">-TtlInSeconds</span></span>
<span data-ttu-id="d6101-159">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="d6101-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="d6101-160">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="d6101-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d6101-161">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="d6101-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d6101-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d6101-163">Obiekt UniqueKeyPolicy typu Microsoft.Azure.Commands.PspsDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d6101-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d6101-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6101-164">-WhatIf</span></span>
<span data-ttu-id="d6101-165">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6101-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6101-166">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6101-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6101-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6101-167">CommonParameters</span></span>
<span data-ttu-id="d6101-168">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6101-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6101-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6101-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6101-170">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6101-170">INPUTS</span></span>

### <span data-ttu-id="d6101-171">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="d6101-172">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="d6101-173">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6101-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="d6101-174">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d6101-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d6101-175">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d6101-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="d6101-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6101-176">OUTPUTS</span></span>

### <span data-ttu-id="d6101-177">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d6101-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d6101-178">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d6101-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d6101-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6101-179">NOTES</span></span>

## <span data-ttu-id="d6101-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6101-180">RELATED LINKS</span></span>
