---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221533"
---
# <span data-ttu-id="3dc76-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="3dc76-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="3dc76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dc76-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc76-103">Pobiera kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3dc76-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3dc76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dc76-104">SYNTAX</span></span>

### <span data-ttu-id="3dc76-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3dc76-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="3dc76-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dc76-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dc76-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3dc76-107">DESCRIPTION</span></span>
<span data-ttu-id="3dc76-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBCollection** Pobiera kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3dc76-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3dc76-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dc76-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc76-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3dc76-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="3dc76-111">Obiekt zasobu zawiera MongoIndexes, _rid, _ts, właściwości _etag.</span><span class="sxs-lookup"><span data-stu-id="3dc76-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="3dc76-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3dc76-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="3dc76-113">W tym przykładzie jest pobierana ShardKey pobrana kolekcja.</span><span class="sxs-lookup"><span data-stu-id="3dc76-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="3dc76-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dc76-114">PARAMETERS</span></span>

### <span data-ttu-id="3dc76-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3dc76-115">-AccountName</span></span>
<span data-ttu-id="3dc76-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3dc76-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3dc76-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3dc76-117">-DatabaseName</span></span>
<span data-ttu-id="3dc76-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3dc76-118">Database name.</span></span>

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

### <span data-ttu-id="3dc76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc76-119">-DefaultProfile</span></span>
<span data-ttu-id="3dc76-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc76-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc76-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3dc76-121">-Name</span></span>
<span data-ttu-id="3dc76-122">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="3dc76-122">Collection name.</span></span>

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

### <span data-ttu-id="3dc76-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3dc76-123">-ParentObject</span></span>
<span data-ttu-id="3dc76-124">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="3dc76-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="3dc76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc76-125">-ResourceGroupName</span></span>
<span data-ttu-id="3dc76-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3dc76-126">Name of resource group.</span></span>

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

### <span data-ttu-id="3dc76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc76-127">CommonParameters</span></span>
<span data-ttu-id="3dc76-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc76-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc76-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc76-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dc76-130">INPUTS</span></span>

### <span data-ttu-id="3dc76-131">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc76-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3dc76-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dc76-132">OUTPUTS</span></span>

### <span data-ttu-id="3dc76-133">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc76-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="3dc76-134">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc76-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3dc76-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dc76-135">NOTES</span></span>

## <span data-ttu-id="3dc76-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dc76-136">RELATED LINKS</span></span>
