---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196827"
---
# <span data-ttu-id="31c15-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="31c15-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="31c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31c15-102">SYNOPSIS</span></span>
<span data-ttu-id="31c15-103">Tworzy nowy wykres Gremlin Graph o formancie GrassDB.</span><span class="sxs-lookup"><span data-stu-id="31c15-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="31c15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31c15-104">SYNTAX</span></span>

### <span data-ttu-id="31c15-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="31c15-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31c15-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c15-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31c15-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="31c15-107">DESCRIPTION</span></span>
<span data-ttu-id="31c15-108">Tworzy nowy wykres Gremlin Graph o formancie GrassDB.</span><span class="sxs-lookup"><span data-stu-id="31c15-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="31c15-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31c15-109">EXAMPLES</span></span>

### <span data-ttu-id="31c15-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31c15-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="31c15-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31c15-111">PARAMETERS</span></span>

### <span data-ttu-id="31c15-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31c15-112">-AccountName</span></span>
<span data-ttu-id="31c15-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="31c15-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="31c15-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="31c15-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="31c15-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="31c15-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="31c15-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31c15-116">-Confirm</span></span>
<span data-ttu-id="31c15-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="31c15-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31c15-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="31c15-119">Obiekt ConflictResolutionPolicy typu PSConflictResolutionPolicy, jeśli jest ustawiony jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="31c15-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c15-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="31c15-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="31c15-121">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="31c15-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="31c15-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="31c15-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="31c15-123">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="31c15-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="31c15-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="31c15-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="31c15-125">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="31c15-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="31c15-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31c15-126">-DatabaseName</span></span>
<span data-ttu-id="31c15-127">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="31c15-127">Database name.</span></span>

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

### <span data-ttu-id="31c15-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c15-128">-DefaultProfile</span></span>
<span data-ttu-id="31c15-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="31c15-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31c15-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-130">-IndexingPolicy</span></span>
<span data-ttu-id="31c15-131">Obiekt zasad indeksowania typu Microsoft.Azure.Commands.Dosdb.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="31c15-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c15-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="31c15-132">-Name</span></span>
<span data-ttu-id="31c15-133">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="31c15-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="31c15-134">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="31c15-134">-ParentObject</span></span>
<span data-ttu-id="31c15-135">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="31c15-135">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c15-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="31c15-136">-PartitionKeyKind</span></span>
<span data-ttu-id="31c15-137">Rodzaj algorytmu używanego do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="31c15-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="31c15-138">Możliwe wartości: "Skrót", "Zakres"</span><span class="sxs-lookup"><span data-stu-id="31c15-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="31c15-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="31c15-139">-PartitionKeyPath</span></span>
<span data-ttu-id="31c15-140">Ścieżka klucza partycji, na przykład "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="31c15-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="31c15-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="31c15-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="31c15-142">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="31c15-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="31c15-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c15-143">-ResourceGroupName</span></span>
<span data-ttu-id="31c15-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31c15-144">Name of resource group.</span></span>

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

### <span data-ttu-id="31c15-145">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="31c15-145">-Throughput</span></span>
<span data-ttu-id="31c15-146">Przepływność wykresu Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="31c15-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="31c15-147">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="31c15-147">Default value is 400.</span></span>

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

### <span data-ttu-id="31c15-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="31c15-148">-TtlInSeconds</span></span>
<span data-ttu-id="31c15-149">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="31c15-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="31c15-150">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="31c15-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="31c15-151">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="31c15-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="31c15-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="31c15-153">Obiekt UniqueKeyPolicy typu Microsoft.Azure.Commands.Dosdb.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="31c15-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c15-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31c15-154">-WhatIf</span></span>
<span data-ttu-id="31c15-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31c15-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31c15-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="31c15-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31c15-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c15-157">CommonParameters</span></span>
<span data-ttu-id="31c15-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c15-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c15-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31c15-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c15-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31c15-160">INPUTS</span></span>

### <span data-ttu-id="31c15-161">Microsoft.Azure.Commands.Dosdb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="31c15-162">Microsoft.Azure.Commands.Dosdb.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="31c15-163">Microsoft.Azure.Commands.DoceńDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="31c15-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="31c15-164">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="31c15-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="31c15-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31c15-165">OUTPUTS</span></span>

### <span data-ttu-id="31c15-166">Microsoft.Azure.Commands.Dosdb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="31c15-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="31c15-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="31c15-167">System.Exception</span></span>

## <span data-ttu-id="31c15-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31c15-168">NOTES</span></span>

## <span data-ttu-id="31c15-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31c15-169">RELATED LINKS</span></span>
