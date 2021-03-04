---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954769"
---
# <span data-ttu-id="131e2-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="131e2-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="131e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="131e2-102">SYNOPSIS</span></span>
<span data-ttu-id="131e2-103">Tworzy nową kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="131e2-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="131e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="131e2-104">SYNTAX</span></span>

### <span data-ttu-id="131e2-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="131e2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131e2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="131e2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="131e2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="131e2-107">DESCRIPTION</span></span>
<span data-ttu-id="131e2-108">Tworzy nową kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="131e2-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="131e2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="131e2-109">EXAMPLES</span></span>

### <span data-ttu-id="131e2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="131e2-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="131e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="131e2-111">PARAMETERS</span></span>

### <span data-ttu-id="131e2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="131e2-112">-AccountName</span></span>
<span data-ttu-id="131e2-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="131e2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="131e2-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="131e2-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="131e2-115">TTL for Analytical Storage (Czas wygaśnięcia dla magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="131e2-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="131e2-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="131e2-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="131e2-117">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="131e2-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="131e2-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="131e2-118">-Confirm</span></span>
<span data-ttu-id="131e2-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="131e2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131e2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="131e2-120">-DatabaseName</span></span>
<span data-ttu-id="131e2-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="131e2-121">Database name.</span></span>

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

### <span data-ttu-id="131e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131e2-122">-DefaultProfile</span></span>
<span data-ttu-id="131e2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="131e2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131e2-124">-Index</span><span class="sxs-lookup"><span data-stu-id="131e2-124">-Index</span></span>
<span data-ttu-id="131e2-125">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="131e2-125">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131e2-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="131e2-126">-Name</span></span>
<span data-ttu-id="131e2-127">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="131e2-127">Collection name.</span></span>

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

### <span data-ttu-id="131e2-128">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="131e2-128">-ParentObject</span></span>
<span data-ttu-id="131e2-129">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="131e2-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="131e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="131e2-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="131e2-131">Name of resource group.</span></span>

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

### <span data-ttu-id="131e2-132">-S s</span><span class="sxs-lookup"><span data-stu-id="131e2-132">-Shard</span></span>
<span data-ttu-id="131e2-133">Ścieżka klucza singa.</span><span class="sxs-lookup"><span data-stu-id="131e2-133">Sharding key path.</span></span>

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

### <span data-ttu-id="131e2-134">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="131e2-134">-Throughput</span></span>
<span data-ttu-id="131e2-135">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="131e2-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="131e2-136">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="131e2-136">Default value is 400.</span></span>

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

### <span data-ttu-id="131e2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131e2-137">-WhatIf</span></span>
<span data-ttu-id="131e2-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="131e2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131e2-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="131e2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131e2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131e2-140">CommonParameters</span></span>
<span data-ttu-id="131e2-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131e2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131e2-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="131e2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131e2-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131e2-143">INPUTS</span></span>

### <span data-ttu-id="131e2-144">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="131e2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="131e2-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131e2-145">OUTPUTS</span></span>

### <span data-ttu-id="131e2-146">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="131e2-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="131e2-147">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="131e2-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="131e2-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="131e2-148">NOTES</span></span>

## <span data-ttu-id="131e2-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="131e2-149">RELATED LINKS</span></span>
