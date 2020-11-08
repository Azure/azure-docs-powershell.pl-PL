---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053086"
---
# <span data-ttu-id="36216-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="36216-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="36216-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36216-102">SYNOPSIS</span></span>
<span data-ttu-id="36216-103">Pobiera kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="36216-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="36216-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36216-104">SYNTAX</span></span>

### <span data-ttu-id="36216-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36216-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="36216-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36216-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36216-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36216-107">DESCRIPTION</span></span>
<span data-ttu-id="36216-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBCollection** Pobiera kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="36216-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="36216-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36216-109">EXAMPLES</span></span>

### <span data-ttu-id="36216-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36216-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="36216-111">Obiekt zasobu zawiera MongoIndexes, _rid, _ts, właściwości _etag.</span><span class="sxs-lookup"><span data-stu-id="36216-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="36216-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36216-112">PARAMETERS</span></span>

### <span data-ttu-id="36216-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36216-113">-AccountName</span></span>
<span data-ttu-id="36216-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="36216-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36216-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36216-115">-DatabaseName</span></span>
<span data-ttu-id="36216-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36216-116">Database name.</span></span>

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

### <span data-ttu-id="36216-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36216-117">-DefaultProfile</span></span>
<span data-ttu-id="36216-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36216-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36216-119">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="36216-119">-Detailed</span></span>
<span data-ttu-id="36216-120">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci kolekcję z odpowiednią wartością przepustowości.</span><span class="sxs-lookup"><span data-stu-id="36216-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36216-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36216-121">-InputObject</span></span>
<span data-ttu-id="36216-122">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="36216-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="36216-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36216-123">-Name</span></span>
<span data-ttu-id="36216-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="36216-124">Collection name.</span></span>

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

### <span data-ttu-id="36216-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36216-125">-ResourceGroupName</span></span>
<span data-ttu-id="36216-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36216-126">Name of resource group.</span></span>

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

### <span data-ttu-id="36216-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36216-127">CommonParameters</span></span>
<span data-ttu-id="36216-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36216-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36216-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36216-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36216-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36216-130">INPUTS</span></span>

### <span data-ttu-id="36216-131">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="36216-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="36216-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36216-132">OUTPUTS</span></span>

### <span data-ttu-id="36216-133">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="36216-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="36216-134">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="36216-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="36216-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36216-135">NOTES</span></span>

## <span data-ttu-id="36216-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36216-136">RELATED LINKS</span></span>
