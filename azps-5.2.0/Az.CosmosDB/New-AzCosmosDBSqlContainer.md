---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355297"
---
# <span data-ttu-id="98e7f-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="98e7f-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="98e7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="98e7f-103">Tworzy nowy kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="98e7f-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="98e7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98e7f-104">SYNTAX</span></span>

### <span data-ttu-id="98e7f-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98e7f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e7f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e7f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98e7f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98e7f-107">DESCRIPTION</span></span>
<span data-ttu-id="98e7f-108">Tworzy nowy kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="98e7f-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="98e7f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98e7f-109">EXAMPLES</span></span>

### <span data-ttu-id="98e7f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98e7f-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="98e7f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98e7f-111">PARAMETERS</span></span>

### <span data-ttu-id="98e7f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98e7f-112">-AccountName</span></span>
<span data-ttu-id="98e7f-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="98e7f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="98e7f-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="98e7f-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="98e7f-115">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="98e7f-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="98e7f-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98e7f-116">-Confirm</span></span>
<span data-ttu-id="98e7f-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e7f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e7f-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="98e7f-119">Obiekt ConflictResolutionPolicy typu PSSqlConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="98e7f-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="98e7f-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="98e7f-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="98e7f-121">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="98e7f-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="98e7f-122">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="98e7f-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="98e7f-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="98e7f-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="98e7f-124">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="98e7f-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="98e7f-125">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="98e7f-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="98e7f-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="98e7f-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="98e7f-127">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="98e7f-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="98e7f-128">Jeśli jest dostarczany wraz z parametrem ConflictResolutionPolicy, jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="98e7f-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="98e7f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98e7f-129">-DatabaseName</span></span>
<span data-ttu-id="98e7f-130">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="98e7f-130">Database name.</span></span>

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

### <span data-ttu-id="98e7f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e7f-131">-DefaultProfile</span></span>
<span data-ttu-id="98e7f-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98e7f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e7f-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-133">-IndexingPolicy</span></span>
<span data-ttu-id="98e7f-134">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="98e7f-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="98e7f-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98e7f-135">-Name</span></span>
<span data-ttu-id="98e7f-136">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="98e7f-136">Container name.</span></span>

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

### <span data-ttu-id="98e7f-137">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="98e7f-137">-ParentObject</span></span>
<span data-ttu-id="98e7f-138">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="98e7f-138">Sql Database object.</span></span>

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

### <span data-ttu-id="98e7f-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="98e7f-139">-PartitionKeyKind</span></span>
<span data-ttu-id="98e7f-140">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="98e7f-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="98e7f-141">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="98e7f-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="98e7f-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="98e7f-142">-PartitionKeyPath</span></span>
<span data-ttu-id="98e7f-143">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="98e7f-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="98e7f-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="98e7f-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="98e7f-145">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="98e7f-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="98e7f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e7f-146">-ResourceGroupName</span></span>
<span data-ttu-id="98e7f-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98e7f-147">Name of resource group.</span></span>

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

### <span data-ttu-id="98e7f-148">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="98e7f-148">-Throughput</span></span>
<span data-ttu-id="98e7f-149">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="98e7f-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="98e7f-150">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="98e7f-150">Default value is 400.</span></span>

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

### <span data-ttu-id="98e7f-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="98e7f-151">-TtlInSeconds</span></span>
<span data-ttu-id="98e7f-152">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="98e7f-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="98e7f-153">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="98e7f-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="98e7f-154">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="98e7f-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="98e7f-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="98e7f-156">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="98e7f-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="98e7f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e7f-157">-WhatIf</span></span>
<span data-ttu-id="98e7f-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e7f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e7f-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98e7f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e7f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e7f-160">CommonParameters</span></span>
<span data-ttu-id="98e7f-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e7f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e7f-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98e7f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e7f-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98e7f-163">INPUTS</span></span>

### <span data-ttu-id="98e7f-164">Microsoft. Azure. Commands. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="98e7f-165">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="98e7f-166">Microsoft. Azure. Commands. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="98e7f-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="98e7f-167">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="98e7f-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="98e7f-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98e7f-168">OUTPUTS</span></span>

### <span data-ttu-id="98e7f-169">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="98e7f-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="98e7f-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="98e7f-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="98e7f-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98e7f-171">NOTES</span></span>

## <span data-ttu-id="98e7f-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98e7f-172">RELATED LINKS</span></span>
