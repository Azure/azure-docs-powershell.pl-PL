---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503836"
---
# <span data-ttu-id="24ccf-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="24ccf-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="24ccf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="24ccf-103">Tworzy nowy wykres Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="24ccf-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="24ccf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24ccf-104">SYNTAX</span></span>

### <span data-ttu-id="24ccf-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24ccf-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ccf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ccf-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24ccf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24ccf-107">DESCRIPTION</span></span>
<span data-ttu-id="24ccf-108">Tworzy nowy wykres Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="24ccf-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="24ccf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24ccf-109">EXAMPLES</span></span>

### <span data-ttu-id="24ccf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24ccf-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="24ccf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24ccf-111">PARAMETERS</span></span>

### <span data-ttu-id="24ccf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24ccf-112">-AccountName</span></span>
<span data-ttu-id="24ccf-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="24ccf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24ccf-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="24ccf-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="24ccf-115">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="24ccf-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="24ccf-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24ccf-116">-Confirm</span></span>
<span data-ttu-id="24ccf-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ccf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ccf-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="24ccf-119">Obiekt ConflictResolutionPolicy typu PSConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="24ccf-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="24ccf-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="24ccf-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="24ccf-121">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="24ccf-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="24ccf-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="24ccf-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="24ccf-123">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="24ccf-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="24ccf-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="24ccf-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="24ccf-125">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="24ccf-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="24ccf-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24ccf-126">-DatabaseName</span></span>
<span data-ttu-id="24ccf-127">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="24ccf-127">Database name.</span></span>

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

### <span data-ttu-id="24ccf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ccf-128">-DefaultProfile</span></span>
<span data-ttu-id="24ccf-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24ccf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ccf-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-130">-IndexingPolicy</span></span>
<span data-ttu-id="24ccf-131">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="24ccf-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="24ccf-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24ccf-132">-Name</span></span>
<span data-ttu-id="24ccf-133">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="24ccf-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="24ccf-134">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="24ccf-134">-ParentObject</span></span>
<span data-ttu-id="24ccf-135">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="24ccf-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="24ccf-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="24ccf-136">-PartitionKeyKind</span></span>
<span data-ttu-id="24ccf-137">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="24ccf-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="24ccf-138">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="24ccf-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="24ccf-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="24ccf-139">-PartitionKeyPath</span></span>
<span data-ttu-id="24ccf-140">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="24ccf-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="24ccf-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="24ccf-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="24ccf-142">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="24ccf-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="24ccf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ccf-143">-ResourceGroupName</span></span>
<span data-ttu-id="24ccf-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24ccf-144">Name of resource group.</span></span>

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

### <span data-ttu-id="24ccf-145">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="24ccf-145">-Throughput</span></span>
<span data-ttu-id="24ccf-146">Przepływność wykresu Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="24ccf-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="24ccf-147">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="24ccf-147">Default value is 400.</span></span>

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

### <span data-ttu-id="24ccf-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="24ccf-148">-TtlInSeconds</span></span>
<span data-ttu-id="24ccf-149">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="24ccf-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="24ccf-150">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="24ccf-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="24ccf-151">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="24ccf-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="24ccf-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="24ccf-153">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="24ccf-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="24ccf-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ccf-154">-WhatIf</span></span>
<span data-ttu-id="24ccf-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ccf-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ccf-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24ccf-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ccf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ccf-157">CommonParameters</span></span>
<span data-ttu-id="24ccf-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ccf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ccf-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24ccf-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ccf-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24ccf-160">INPUTS</span></span>

### <span data-ttu-id="24ccf-161">Microsoft. Azure. Commands. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="24ccf-162">Microsoft. Azure. Commands. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="24ccf-163">Microsoft. Azure. Commands. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ccf-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="24ccf-164">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="24ccf-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="24ccf-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24ccf-165">OUTPUTS</span></span>

### <span data-ttu-id="24ccf-166">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="24ccf-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="24ccf-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="24ccf-167">System.Exception</span></span>

## <span data-ttu-id="24ccf-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24ccf-168">NOTES</span></span>

## <span data-ttu-id="24ccf-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24ccf-169">RELATED LINKS</span></span>
