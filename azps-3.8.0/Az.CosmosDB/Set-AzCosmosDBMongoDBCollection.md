---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053403"
---
# <span data-ttu-id="11c33-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="11c33-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="11c33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11c33-102">SYNOPSIS</span></span>
<span data-ttu-id="11c33-103">Ustawia kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11c33-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="11c33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11c33-104">SYNTAX</span></span>

### <span data-ttu-id="11c33-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11c33-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c33-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c33-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c33-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11c33-107">DESCRIPTION</span></span>
<span data-ttu-id="11c33-108">Polecenie cmdlet **Set-AzCosmosDBMongoDBCollection** ustawia kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11c33-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="11c33-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11c33-109">EXAMPLES</span></span>

### <span data-ttu-id="11c33-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11c33-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="11c33-111">Obiekt zasobu zawiera MongoIndexes, _rid, _ts, właściwości _etag.</span><span class="sxs-lookup"><span data-stu-id="11c33-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="11c33-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11c33-112">PARAMETERS</span></span>

### <span data-ttu-id="11c33-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11c33-113">-AccountName</span></span>
<span data-ttu-id="11c33-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="11c33-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11c33-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11c33-115">-Confirm</span></span>
<span data-ttu-id="11c33-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c33-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c33-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11c33-117">-DatabaseName</span></span>
<span data-ttu-id="11c33-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="11c33-118">Database name.</span></span>

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

### <span data-ttu-id="11c33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c33-119">-DefaultProfile</span></span>
<span data-ttu-id="11c33-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11c33-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c33-121">-Index</span><span class="sxs-lookup"><span data-stu-id="11c33-121">-Index</span></span>
<span data-ttu-id="11c33-122">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="11c33-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="11c33-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11c33-123">-InputObject</span></span>
<span data-ttu-id="11c33-124">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="11c33-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="11c33-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11c33-125">-Name</span></span>
<span data-ttu-id="11c33-126">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="11c33-126">Collection name.</span></span>

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

### <span data-ttu-id="11c33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c33-127">-ResourceGroupName</span></span>
<span data-ttu-id="11c33-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11c33-128">Name of resource group.</span></span>

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

### <span data-ttu-id="11c33-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="11c33-129">-Shard</span></span>
<span data-ttu-id="11c33-130">Ścieżka klucza sharding.</span><span class="sxs-lookup"><span data-stu-id="11c33-130">Sharding key path.</span></span>

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

### <span data-ttu-id="11c33-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="11c33-131">-Throughput</span></span>
<span data-ttu-id="11c33-132">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="11c33-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="11c33-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="11c33-133">Default value is 400.</span></span>

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

### <span data-ttu-id="11c33-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c33-134">-WhatIf</span></span>
<span data-ttu-id="11c33-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c33-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c33-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11c33-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c33-137">CommonParameters</span></span>
<span data-ttu-id="11c33-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c33-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11c33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c33-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11c33-140">INPUTS</span></span>

### <span data-ttu-id="11c33-141">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="11c33-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="11c33-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11c33-142">OUTPUTS</span></span>

### <span data-ttu-id="11c33-143">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="11c33-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="11c33-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11c33-144">NOTES</span></span>

## <span data-ttu-id="11c33-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11c33-145">RELATED LINKS</span></span>
