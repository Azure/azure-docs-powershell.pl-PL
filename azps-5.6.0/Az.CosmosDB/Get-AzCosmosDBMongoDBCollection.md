---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: bb73bd88abf677f9855d934a995f3f9107e44b4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978730"
---
# <span data-ttu-id="b4832-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b4832-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b4832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4832-102">SYNOPSIS</span></span>
<span data-ttu-id="b4832-103">Pobiera kolekcję Bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b4832-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b4832-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4832-104">SYNTAX</span></span>

### <span data-ttu-id="b4832-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4832-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b4832-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4832-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4832-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4832-107">DESCRIPTION</span></span>
<span data-ttu-id="b4832-108">Polecenie **cmdlet Get-AzCosmosDBMongoDBCollection** pobiera kolekcję Dosdb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b4832-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b4832-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4832-109">EXAMPLES</span></span>

### <span data-ttu-id="b4832-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4832-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="b4832-111">Obiekt zasobu zawiera indeksy MongoIndexes, _rid, _ts, _etag właściwości.</span><span class="sxs-lookup"><span data-stu-id="b4832-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="b4832-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4832-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="b4832-113">W tym przykładzie jest pobierany klucz Skey z pobranej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b4832-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="b4832-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4832-114">PARAMETERS</span></span>

### <span data-ttu-id="b4832-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4832-115">-AccountName</span></span>
<span data-ttu-id="b4832-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b4832-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4832-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4832-117">-DatabaseName</span></span>
<span data-ttu-id="b4832-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b4832-118">Database name.</span></span>

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

### <span data-ttu-id="b4832-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4832-119">-DefaultProfile</span></span>
<span data-ttu-id="b4832-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4832-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4832-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4832-121">-Name</span></span>
<span data-ttu-id="b4832-122">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b4832-122">Collection name.</span></span>

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

### <span data-ttu-id="b4832-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4832-123">-ParentObject</span></span>
<span data-ttu-id="b4832-124">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="b4832-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="b4832-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4832-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4832-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4832-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b4832-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4832-127">CommonParameters</span></span>
<span data-ttu-id="b4832-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4832-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4832-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4832-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4832-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4832-130">INPUTS</span></span>

### <span data-ttu-id="b4832-131">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b4832-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="b4832-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4832-132">OUTPUTS</span></span>

### <span data-ttu-id="b4832-133">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="b4832-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="b4832-134">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b4832-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b4832-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4832-135">NOTES</span></span>

## <span data-ttu-id="b4832-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4832-136">RELATED LINKS</span></span>
