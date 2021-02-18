---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181266"
---
# <span data-ttu-id="899bf-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="899bf-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="899bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899bf-102">SYNOPSIS</span></span>
<span data-ttu-id="899bf-103">Aktualizacja wykresu Gremlin Graph dla gry GrysDB.</span><span class="sxs-lookup"><span data-stu-id="899bf-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="899bf-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący wykres.</span><span class="sxs-lookup"><span data-stu-id="899bf-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="899bf-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="899bf-105">SYNTAX</span></span>

### <span data-ttu-id="899bf-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="899bf-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="899bf-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="899bf-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="899bf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="899bf-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="899bf-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="899bf-109">DESCRIPTION</span></span>
<span data-ttu-id="899bf-110">Aktualizacja wykresu Gremlin Graph dla gry GrysDB.</span><span class="sxs-lookup"><span data-stu-id="899bf-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="899bf-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejący wykres.</span><span class="sxs-lookup"><span data-stu-id="899bf-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="899bf-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="899bf-112">EXAMPLES</span></span>

### <span data-ttu-id="899bf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="899bf-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="899bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="899bf-114">PARAMETERS</span></span>

### <span data-ttu-id="899bf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="899bf-115">-AccountName</span></span>
<span data-ttu-id="899bf-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="899bf-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="899bf-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="899bf-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="899bf-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="899bf-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="899bf-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="899bf-119">-Confirm</span></span>
<span data-ttu-id="899bf-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="899bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899bf-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="899bf-122">Obiekt ConflictResolutionPolicy typu PSConflictResolutionPolicy, jeśli jest ustawiony jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="899bf-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="899bf-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="899bf-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="899bf-124">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="899bf-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="899bf-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="899bf-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="899bf-126">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="899bf-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="899bf-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="899bf-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="899bf-128">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="899bf-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="899bf-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="899bf-129">-DatabaseName</span></span>
<span data-ttu-id="899bf-130">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="899bf-130">Database name.</span></span>

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

### <span data-ttu-id="899bf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899bf-131">-DefaultProfile</span></span>
<span data-ttu-id="899bf-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="899bf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="899bf-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-133">-IndexingPolicy</span></span>
<span data-ttu-id="899bf-134">Obiekt zasad indeksowania typu Microsoft.Azure.Commands.Dosdb.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="899bf-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="899bf-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="899bf-135">-InputObject</span></span>
<span data-ttu-id="899bf-136">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="899bf-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="899bf-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="899bf-137">-Name</span></span>
<span data-ttu-id="899bf-138">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="899bf-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="899bf-139">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="899bf-139">-ParentObject</span></span>
<span data-ttu-id="899bf-140">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="899bf-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="899bf-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="899bf-141">-PartitionKeyKind</span></span>
<span data-ttu-id="899bf-142">Rodzaj algorytmu używanego do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="899bf-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="899bf-143">Możliwe wartości: "Skrót", "Zakres"</span><span class="sxs-lookup"><span data-stu-id="899bf-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="899bf-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="899bf-144">-PartitionKeyPath</span></span>
<span data-ttu-id="899bf-145">Ścieżka klucza partycji, na przykład "/address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="899bf-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="899bf-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="899bf-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="899bf-147">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="899bf-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="899bf-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899bf-148">-ResourceGroupName</span></span>
<span data-ttu-id="899bf-149">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="899bf-149">Name of resource group.</span></span>

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

### <span data-ttu-id="899bf-150">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="899bf-150">-Throughput</span></span>
<span data-ttu-id="899bf-151">Przepływność wykresu Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="899bf-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="899bf-152">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="899bf-152">Default value is 400.</span></span>

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

### <span data-ttu-id="899bf-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="899bf-153">-TtlInSeconds</span></span>
<span data-ttu-id="899bf-154">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="899bf-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="899bf-155">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="899bf-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="899bf-156">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="899bf-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="899bf-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="899bf-158">Obiekt UniqueKeyPolicy typu Microsoft.Azure.Commands.PspsDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="899bf-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="899bf-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899bf-159">-WhatIf</span></span>
<span data-ttu-id="899bf-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="899bf-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899bf-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="899bf-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="899bf-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899bf-162">CommonParameters</span></span>
<span data-ttu-id="899bf-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899bf-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899bf-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="899bf-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899bf-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="899bf-165">INPUTS</span></span>

### <span data-ttu-id="899bf-166">Microsoft.Azure.Commands.Dosdb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="899bf-167">Microsoft.Azure.Commands.Dosdb.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="899bf-168">Microsoft.Azure.Commands.DoceńDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="899bf-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="899bf-169">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="899bf-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="899bf-170">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="899bf-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="899bf-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="899bf-171">OUTPUTS</span></span>

### <span data-ttu-id="899bf-172">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="899bf-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="899bf-173">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="899bf-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="899bf-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="899bf-174">NOTES</span></span>

## <span data-ttu-id="899bf-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="899bf-175">RELATED LINKS</span></span>
