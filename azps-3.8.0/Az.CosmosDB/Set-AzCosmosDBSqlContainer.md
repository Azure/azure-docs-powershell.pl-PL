---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053391"
---
# <span data-ttu-id="63f93-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="63f93-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="63f93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63f93-102">SYNOPSIS</span></span>
<span data-ttu-id="63f93-103">Tworzy nowy lub aktualizuje istniejący kontener SQL programu CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="63f93-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="63f93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63f93-104">SYNTAX</span></span>

### <span data-ttu-id="63f93-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63f93-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f93-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f93-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f93-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63f93-107">DESCRIPTION</span></span>
<span data-ttu-id="63f93-108">Polecenie cmdlet **Set-AzCosmosDBSqlContainer** tworzy nowy lub aktualizuje istniejący kontener SQL programu CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="63f93-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="63f93-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63f93-109">EXAMPLES</span></span>

### <span data-ttu-id="63f93-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63f93-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="63f93-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63f93-111">PARAMETERS</span></span>

### <span data-ttu-id="63f93-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63f93-112">-AccountName</span></span>
<span data-ttu-id="63f93-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="63f93-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63f93-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63f93-114">-Confirm</span></span>
<span data-ttu-id="63f93-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f93-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f93-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="63f93-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="63f93-117">Obiekt ConflictResolutionPolicy typu PSSqlConflictResolutionPolicy, gdy jest to określone jako ConflictResolutionPolicy kontenera.</span><span class="sxs-lookup"><span data-stu-id="63f93-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="63f93-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="63f93-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="63f93-119">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="63f93-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="63f93-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="63f93-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="63f93-121">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="63f93-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="63f93-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="63f93-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="63f93-123">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="63f93-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="63f93-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63f93-124">-DatabaseName</span></span>
<span data-ttu-id="63f93-125">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="63f93-125">Database name.</span></span>

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

### <span data-ttu-id="63f93-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f93-126">-DefaultProfile</span></span>
<span data-ttu-id="63f93-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63f93-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f93-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="63f93-128">-IndexingPolicy</span></span>
<span data-ttu-id="63f93-129">Obiekt zasad indeksowania typu Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="63f93-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="63f93-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63f93-130">-InputObject</span></span>
<span data-ttu-id="63f93-131">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="63f93-131">Sql Database object.</span></span>

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

### <span data-ttu-id="63f93-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63f93-132">-Name</span></span>
<span data-ttu-id="63f93-133">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="63f93-133">Container name.</span></span>

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

### <span data-ttu-id="63f93-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="63f93-134">-PartitionKeyKind</span></span>
<span data-ttu-id="63f93-135">Rodzaj algorytmu używany do partycjonowania.</span><span class="sxs-lookup"><span data-stu-id="63f93-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="63f93-136">Możliwe są następujące wartości: "hash", "Range"</span><span class="sxs-lookup"><span data-stu-id="63f93-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="63f93-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="63f93-137">-PartitionKeyPath</span></span>
<span data-ttu-id="63f93-138">Ścieżka klucza partycji, na przykład "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="63f93-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="63f93-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="63f93-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="63f93-140">Wersja definicji klucza partycji</span><span class="sxs-lookup"><span data-stu-id="63f93-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="63f93-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f93-141">-ResourceGroupName</span></span>
<span data-ttu-id="63f93-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63f93-142">Name of resource group.</span></span>

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

### <span data-ttu-id="63f93-143">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="63f93-143">-Throughput</span></span>
<span data-ttu-id="63f93-144">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="63f93-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="63f93-145">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="63f93-145">Default value is 400.</span></span>

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

### <span data-ttu-id="63f93-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="63f93-146">-TtlInSeconds</span></span>
<span data-ttu-id="63f93-147">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="63f93-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="63f93-148">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="63f93-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="63f93-149">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="63f93-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="63f93-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="63f93-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="63f93-151">Obiekt UniqueKeyPolicy typu Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="63f93-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="63f93-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f93-152">-WhatIf</span></span>
<span data-ttu-id="63f93-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f93-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63f93-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63f93-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f93-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f93-155">CommonParameters</span></span>
<span data-ttu-id="63f93-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f93-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f93-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63f93-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f93-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63f93-158">INPUTS</span></span>

### <span data-ttu-id="63f93-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="63f93-159">None</span></span>

## <span data-ttu-id="63f93-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63f93-160">OUTPUTS</span></span>

### <span data-ttu-id="63f93-161">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="63f93-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="63f93-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63f93-162">NOTES</span></span>

## <span data-ttu-id="63f93-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63f93-163">RELATED LINKS</span></span>
