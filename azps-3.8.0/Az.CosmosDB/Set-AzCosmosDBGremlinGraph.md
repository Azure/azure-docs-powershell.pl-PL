---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053404"
---
# <span data-ttu-id="24985-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="24985-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="24985-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24985-102">SYNOPSIS</span></span>
<span data-ttu-id="24985-103">Ustawia wykres Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="24985-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="24985-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24985-104">SYNTAX</span></span>

### <span data-ttu-id="24985-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24985-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24985-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24985-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24985-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24985-107">DESCRIPTION</span></span>
<span data-ttu-id="24985-108">Polecenie cmdlet **Set-AzCosmosDBGremlinGraph** ustawia CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="24985-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="24985-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24985-109">EXAMPLES</span></span>

### <span data-ttu-id="24985-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24985-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="24985-111">Obiekt zasobu zawiera IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="24985-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="24985-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24985-112">PARAMETERS</span></span>

### <span data-ttu-id="24985-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24985-113">-AccountName</span></span>
<span data-ttu-id="24985-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="24985-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24985-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24985-115">-Confirm</span></span>
<span data-ttu-id="24985-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24985-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24985-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="24985-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="24985-118">Obiekt ConflictResolutionPolicy typu PSConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="24985-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="24985-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="24985-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="24985-120">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="24985-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="24985-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="24985-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="24985-122">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="24985-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="24985-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="24985-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="24985-124">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="24985-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="24985-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24985-125">-DatabaseName</span></span>
<span data-ttu-id="24985-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="24985-126">Database name.</span></span>

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

### <span data-ttu-id="24985-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24985-127">-DefaultProfile</span></span>
<span data-ttu-id="24985-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24985-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24985-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="24985-129">-IndexingPolicy</span></span>
<span data-ttu-id="24985-130">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="24985-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="24985-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24985-131">-InputObject</span></span>
<span data-ttu-id="24985-132">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="24985-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="24985-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24985-133">-Name</span></span>
<span data-ttu-id="24985-134">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="24985-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="24985-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="24985-135">-PartitionKeyKind</span></span>
<span data-ttu-id="24985-136">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="24985-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="24985-137">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="24985-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="24985-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="24985-138">-PartitionKeyPath</span></span>
<span data-ttu-id="24985-139">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="24985-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="24985-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="24985-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="24985-141">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="24985-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="24985-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24985-142">-ResourceGroupName</span></span>
<span data-ttu-id="24985-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24985-143">Name of resource group.</span></span>

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

### <span data-ttu-id="24985-144">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="24985-144">-Throughput</span></span>
<span data-ttu-id="24985-145">Przepływność wykresu Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="24985-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="24985-146">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="24985-146">Default value is 400.</span></span>

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

### <span data-ttu-id="24985-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="24985-147">-TtlInSeconds</span></span>
<span data-ttu-id="24985-148">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="24985-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="24985-149">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="24985-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="24985-150">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="24985-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="24985-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="24985-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="24985-152">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="24985-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="24985-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24985-153">-WhatIf</span></span>
<span data-ttu-id="24985-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24985-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24985-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24985-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24985-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24985-156">CommonParameters</span></span>
<span data-ttu-id="24985-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24985-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24985-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24985-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24985-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24985-159">INPUTS</span></span>

### <span data-ttu-id="24985-160">Microsoft. Azure. Commands. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="24985-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="24985-161">Microsoft. Azure. Commands. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="24985-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="24985-162">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="24985-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="24985-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24985-163">OUTPUTS</span></span>

### <span data-ttu-id="24985-164">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="24985-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="24985-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24985-165">NOTES</span></span>

## <span data-ttu-id="24985-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24985-166">RELATED LINKS</span></span>
