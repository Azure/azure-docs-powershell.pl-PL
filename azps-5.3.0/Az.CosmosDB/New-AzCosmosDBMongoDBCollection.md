---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503824"
---
# <span data-ttu-id="e3ae4-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="e3ae4-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="e3ae4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ae4-103">Tworzy nową kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="e3ae4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3ae4-104">SYNTAX</span></span>

### <span data-ttu-id="e3ae4-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e3ae4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ae4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3ae4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3ae4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ae4-108">Tworzy nową kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="e3ae4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3ae4-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ae4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3ae4-110">Example 1</span></span>
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

## <span data-ttu-id="e3ae4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3ae4-111">PARAMETERS</span></span>

### <span data-ttu-id="e3ae4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3ae4-112">-AccountName</span></span>
<span data-ttu-id="e3ae4-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3ae4-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="e3ae4-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="e3ae4-115">Czas wygaśnięcia (TTL) dla magazynu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="e3ae4-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e3ae4-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e3ae4-117">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e3ae4-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3ae4-118">-Confirm</span></span>
<span data-ttu-id="e3ae4-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ae4-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3ae4-120">-DatabaseName</span></span>
<span data-ttu-id="e3ae4-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-121">Database name.</span></span>

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

### <span data-ttu-id="e3ae4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ae4-122">-DefaultProfile</span></span>
<span data-ttu-id="e3ae4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ae4-124">-Index</span><span class="sxs-lookup"><span data-stu-id="e3ae4-124">-Index</span></span>
<span data-ttu-id="e3ae4-125">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="e3ae4-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3ae4-126">-Name</span></span>
<span data-ttu-id="e3ae4-127">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-127">Collection name.</span></span>

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

### <span data-ttu-id="e3ae4-128">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e3ae4-128">-ParentObject</span></span>
<span data-ttu-id="e3ae4-129">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="e3ae4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ae4-130">-ResourceGroupName</span></span>
<span data-ttu-id="e3ae4-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-131">Name of resource group.</span></span>

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

### <span data-ttu-id="e3ae4-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="e3ae4-132">-Shard</span></span>
<span data-ttu-id="e3ae4-133">Ścieżka klucza sharding.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-133">Sharding key path.</span></span>

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

### <span data-ttu-id="e3ae4-134">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="e3ae4-134">-Throughput</span></span>
<span data-ttu-id="e3ae4-135">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e3ae4-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="e3ae4-136">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-136">Default value is 400.</span></span>

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

### <span data-ttu-id="e3ae4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ae4-137">-WhatIf</span></span>
<span data-ttu-id="e3ae4-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ae4-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ae4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ae4-140">CommonParameters</span></span>
<span data-ttu-id="e3ae4-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ae4-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3ae4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ae4-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3ae4-143">INPUTS</span></span>

### <span data-ttu-id="e3ae4-144">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e3ae4-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="e3ae4-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3ae4-145">OUTPUTS</span></span>

### <span data-ttu-id="e3ae4-146">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="e3ae4-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="e3ae4-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e3ae4-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e3ae4-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3ae4-148">NOTES</span></span>

## <span data-ttu-id="e3ae4-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3ae4-149">RELATED LINKS</span></span>
