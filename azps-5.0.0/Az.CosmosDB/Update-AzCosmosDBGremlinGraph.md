---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306804"
---
# <span data-ttu-id="6acbf-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="6acbf-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="6acbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6acbf-102">SYNOPSIS</span></span>
<span data-ttu-id="6acbf-103">Umożliwia zaktualizowanie wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6acbf-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="6acbf-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący wykres.</span><span class="sxs-lookup"><span data-stu-id="6acbf-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="6acbf-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6acbf-105">SYNTAX</span></span>

### <span data-ttu-id="6acbf-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6acbf-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6acbf-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6acbf-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6acbf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6acbf-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6acbf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6acbf-109">DESCRIPTION</span></span>
<span data-ttu-id="6acbf-110">Umożliwia zaktualizowanie wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6acbf-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="6acbf-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejący wykres.</span><span class="sxs-lookup"><span data-stu-id="6acbf-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="6acbf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6acbf-112">EXAMPLES</span></span>

### <span data-ttu-id="6acbf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6acbf-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="6acbf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6acbf-114">PARAMETERS</span></span>

### <span data-ttu-id="6acbf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6acbf-115">-AccountName</span></span>
<span data-ttu-id="6acbf-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6acbf-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6acbf-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6acbf-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6acbf-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="6acbf-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6acbf-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6acbf-119">-Confirm</span></span>
<span data-ttu-id="6acbf-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acbf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acbf-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="6acbf-122">Obiekt ConflictResolutionPolicy typu PSConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="6acbf-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="6acbf-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="6acbf-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="6acbf-124">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="6acbf-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="6acbf-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="6acbf-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="6acbf-126">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="6acbf-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="6acbf-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="6acbf-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="6acbf-128">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="6acbf-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="6acbf-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6acbf-129">-DatabaseName</span></span>
<span data-ttu-id="6acbf-130">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6acbf-130">Database name.</span></span>

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

### <span data-ttu-id="6acbf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acbf-131">-DefaultProfile</span></span>
<span data-ttu-id="6acbf-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6acbf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6acbf-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-133">-IndexingPolicy</span></span>
<span data-ttu-id="6acbf-134">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="6acbf-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="6acbf-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6acbf-135">-InputObject</span></span>
<span data-ttu-id="6acbf-136">Obiekt wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6acbf-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="6acbf-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6acbf-137">-Name</span></span>
<span data-ttu-id="6acbf-138">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6acbf-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6acbf-139">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6acbf-139">-ParentObject</span></span>
<span data-ttu-id="6acbf-140">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6acbf-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="6acbf-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="6acbf-141">-PartitionKeyKind</span></span>
<span data-ttu-id="6acbf-142">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="6acbf-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="6acbf-143">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="6acbf-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="6acbf-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="6acbf-144">-PartitionKeyPath</span></span>
<span data-ttu-id="6acbf-145">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="6acbf-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="6acbf-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="6acbf-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="6acbf-147">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="6acbf-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="6acbf-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acbf-148">-ResourceGroupName</span></span>
<span data-ttu-id="6acbf-149">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6acbf-149">Name of resource group.</span></span>

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

### <span data-ttu-id="6acbf-150">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="6acbf-150">-Throughput</span></span>
<span data-ttu-id="6acbf-151">Przepływność wykresu Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6acbf-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="6acbf-152">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="6acbf-152">Default value is 400.</span></span>

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

### <span data-ttu-id="6acbf-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6acbf-153">-TtlInSeconds</span></span>
<span data-ttu-id="6acbf-154">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="6acbf-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="6acbf-155">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="6acbf-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="6acbf-156">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="6acbf-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="6acbf-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="6acbf-158">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="6acbf-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="6acbf-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acbf-159">-WhatIf</span></span>
<span data-ttu-id="6acbf-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acbf-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6acbf-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6acbf-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6acbf-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acbf-162">CommonParameters</span></span>
<span data-ttu-id="6acbf-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6acbf-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acbf-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6acbf-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acbf-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6acbf-165">INPUTS</span></span>

### <span data-ttu-id="6acbf-166">Microsoft. Azure. Commands. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="6acbf-167">Microsoft. Azure. Commands. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="6acbf-168">Microsoft. Azure. Commands. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6acbf-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="6acbf-169">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6acbf-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="6acbf-170">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6acbf-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="6acbf-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6acbf-171">OUTPUTS</span></span>

### <span data-ttu-id="6acbf-172">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6acbf-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="6acbf-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="6acbf-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="6acbf-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6acbf-174">NOTES</span></span>

## <span data-ttu-id="6acbf-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6acbf-175">RELATED LINKS</span></span>
