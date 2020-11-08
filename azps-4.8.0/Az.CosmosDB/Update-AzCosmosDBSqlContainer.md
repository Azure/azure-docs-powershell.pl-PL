---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224040"
---
# <span data-ttu-id="b9b3f-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="b9b3f-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="b9b3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b3f-103">Aktualizuje kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="b9b3f-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący kontener.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="b9b3f-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9b3f-105">SYNTAX</span></span>

### <span data-ttu-id="b9b3f-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9b3f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b3f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9b3f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b3f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9b3f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b3f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b9b3f-109">DESCRIPTION</span></span>
<span data-ttu-id="b9b3f-110">Aktualizuje kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="b9b3f-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący kontener.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="b9b3f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9b3f-112">EXAMPLES</span></span>

### <span data-ttu-id="b9b3f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9b3f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="b9b3f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9b3f-114">PARAMETERS</span></span>

### <span data-ttu-id="b9b3f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9b3f-115">-AccountName</span></span>
<span data-ttu-id="b9b3f-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b9b3f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b9b3f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b9b3f-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b9b3f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9b3f-119">-Confirm</span></span>
<span data-ttu-id="b9b3f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b3f-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="b9b3f-122">Obiekt ConflictResolutionPolicy typu PSSqlConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="b9b3f-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="b9b3f-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="b9b3f-124">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="b9b3f-125">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="b9b3f-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="b9b3f-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="b9b3f-127">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="b9b3f-128">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="b9b3f-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="b9b3f-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="b9b3f-130">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="b9b3f-131">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="b9b3f-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9b3f-132">-DatabaseName</span></span>
<span data-ttu-id="b9b3f-133">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-133">Database name.</span></span>

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

### <span data-ttu-id="b9b3f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b3f-134">-DefaultProfile</span></span>
<span data-ttu-id="b9b3f-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b3f-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-136">-IndexingPolicy</span></span>
<span data-ttu-id="b9b3f-137">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="b9b3f-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9b3f-138">-InputObject</span></span>
<span data-ttu-id="b9b3f-139">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-139">Sql Container object.</span></span>

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

### <span data-ttu-id="b9b3f-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9b3f-140">-Name</span></span>
<span data-ttu-id="b9b3f-141">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-141">Container name.</span></span>

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

### <span data-ttu-id="b9b3f-142">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b9b3f-142">-ParentObject</span></span>
<span data-ttu-id="b9b3f-143">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-143">Sql Database object.</span></span>

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

### <span data-ttu-id="b9b3f-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="b9b3f-144">-PartitionKeyKind</span></span>
<span data-ttu-id="b9b3f-145">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="b9b3f-146">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="b9b3f-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="b9b3f-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="b9b3f-147">-PartitionKeyPath</span></span>
<span data-ttu-id="b9b3f-148">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="b9b3f-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="b9b3f-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b9b3f-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="b9b3f-150">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="b9b3f-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="b9b3f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b3f-151">-ResourceGroupName</span></span>
<span data-ttu-id="b9b3f-152">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-152">Name of resource group.</span></span>

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

### <span data-ttu-id="b9b3f-153">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="b9b3f-153">-Throughput</span></span>
<span data-ttu-id="b9b3f-154">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b9b3f-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="b9b3f-155">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-155">Default value is 400.</span></span>

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

### <span data-ttu-id="b9b3f-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="b9b3f-156">-TtlInSeconds</span></span>
<span data-ttu-id="b9b3f-157">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="b9b3f-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="b9b3f-158">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="b9b3f-159">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="b9b3f-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="b9b3f-161">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="b9b3f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b3f-162">-WhatIf</span></span>
<span data-ttu-id="b9b3f-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b3f-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b3f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b3f-165">CommonParameters</span></span>
<span data-ttu-id="b9b3f-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b3f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b3f-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9b3f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b3f-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9b3f-168">INPUTS</span></span>

### <span data-ttu-id="b9b3f-169">Microsoft. Azure. Commands. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="b9b3f-170">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="b9b3f-171">Microsoft. Azure. Commands. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9b3f-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="b9b3f-172">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b9b3f-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b9b3f-173">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="b9b3f-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="b9b3f-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9b3f-174">OUTPUTS</span></span>

### <span data-ttu-id="b9b3f-175">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b9b3f-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b9b3f-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b9b3f-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b9b3f-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9b3f-177">NOTES</span></span>

## <span data-ttu-id="b9b3f-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9b3f-178">RELATED LINKS</span></span>
