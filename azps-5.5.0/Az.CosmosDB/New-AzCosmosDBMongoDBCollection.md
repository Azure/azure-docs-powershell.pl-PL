---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181314"
---
# <span data-ttu-id="5a17f-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5a17f-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5a17f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a17f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a17f-103">Tworzy nową kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="5a17f-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5a17f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a17f-104">SYNTAX</span></span>

### <span data-ttu-id="5a17f-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a17f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a17f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a17f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a17f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a17f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a17f-108">Tworzy nową kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="5a17f-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5a17f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a17f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a17f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a17f-110">Example 1</span></span>
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

## <span data-ttu-id="5a17f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a17f-111">PARAMETERS</span></span>

### <span data-ttu-id="5a17f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a17f-112">-AccountName</span></span>
<span data-ttu-id="5a17f-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="5a17f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a17f-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="5a17f-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5a17f-115">TTL for Analytical Storage (Czas wygaśnięcia dla magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="5a17f-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="5a17f-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5a17f-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5a17f-117">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="5a17f-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5a17f-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a17f-118">-Confirm</span></span>
<span data-ttu-id="5a17f-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a17f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a17f-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a17f-120">-DatabaseName</span></span>
<span data-ttu-id="5a17f-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5a17f-121">Database name.</span></span>

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

### <span data-ttu-id="5a17f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a17f-122">-DefaultProfile</span></span>
<span data-ttu-id="5a17f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a17f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a17f-124">-Index</span><span class="sxs-lookup"><span data-stu-id="5a17f-124">-Index</span></span>
<span data-ttu-id="5a17f-125">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="5a17f-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="5a17f-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a17f-126">-Name</span></span>
<span data-ttu-id="5a17f-127">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="5a17f-127">Collection name.</span></span>

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

### <span data-ttu-id="5a17f-128">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a17f-128">-ParentObject</span></span>
<span data-ttu-id="5a17f-129">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="5a17f-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="5a17f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a17f-130">-ResourceGroupName</span></span>
<span data-ttu-id="5a17f-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a17f-131">Name of resource group.</span></span>

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

### <span data-ttu-id="5a17f-132">-S s</span><span class="sxs-lookup"><span data-stu-id="5a17f-132">-Shard</span></span>
<span data-ttu-id="5a17f-133">Ścieżka klucza singa.</span><span class="sxs-lookup"><span data-stu-id="5a17f-133">Sharding key path.</span></span>

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

### <span data-ttu-id="5a17f-134">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="5a17f-134">-Throughput</span></span>
<span data-ttu-id="5a17f-135">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5a17f-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="5a17f-136">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="5a17f-136">Default value is 400.</span></span>

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

### <span data-ttu-id="5a17f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a17f-137">-WhatIf</span></span>
<span data-ttu-id="5a17f-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a17f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a17f-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a17f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a17f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a17f-140">CommonParameters</span></span>
<span data-ttu-id="5a17f-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a17f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a17f-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a17f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a17f-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a17f-143">INPUTS</span></span>

### <span data-ttu-id="5a17f-144">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5a17f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5a17f-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a17f-145">OUTPUTS</span></span>

### <span data-ttu-id="5a17f-146">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5a17f-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5a17f-147">Microsoft.Azure.Commands.Dosdb.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5a17f-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5a17f-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a17f-148">NOTES</span></span>

## <span data-ttu-id="5a17f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a17f-149">RELATED LINKS</span></span>
