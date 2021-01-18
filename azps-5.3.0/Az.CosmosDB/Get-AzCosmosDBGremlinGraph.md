---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503866"
---
# <span data-ttu-id="f7d61-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f7d61-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f7d61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7d61-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d61-103">Pobiera wykres Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f7d61-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f7d61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7d61-104">SYNTAX</span></span>

### <span data-ttu-id="f7d61-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7d61-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="f7d61-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7d61-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7d61-107">DESCRIPTION</span></span>
<span data-ttu-id="f7d61-108">Polecenie cmdlet **Get-AzCosmosDBGremlinGraph** pobiera właściwości CosmosDB Gremlin wykresu.</span><span class="sxs-lookup"><span data-stu-id="f7d61-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="f7d61-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7d61-109">EXAMPLES</span></span>

### <span data-ttu-id="f7d61-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7d61-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="f7d61-111">Obiekt zasobu zawiera IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="f7d61-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="f7d61-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7d61-112">PARAMETERS</span></span>

### <span data-ttu-id="f7d61-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7d61-113">-AccountName</span></span>
<span data-ttu-id="f7d61-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f7d61-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7d61-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7d61-115">-DatabaseName</span></span>
<span data-ttu-id="f7d61-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f7d61-116">Database name.</span></span>

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

### <span data-ttu-id="f7d61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d61-117">-DefaultProfile</span></span>
<span data-ttu-id="f7d61-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d61-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7d61-119">-Name</span></span>
<span data-ttu-id="f7d61-120">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f7d61-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f7d61-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="f7d61-121">-ParentObject</span></span>
<span data-ttu-id="f7d61-122">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f7d61-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f7d61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d61-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7d61-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7d61-124">Name of resource group.</span></span>

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

### <span data-ttu-id="f7d61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d61-125">CommonParameters</span></span>
<span data-ttu-id="f7d61-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d61-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d61-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d61-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7d61-128">INPUTS</span></span>

### <span data-ttu-id="f7d61-129">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f7d61-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f7d61-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7d61-130">OUTPUTS</span></span>

### <span data-ttu-id="f7d61-131">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f7d61-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f7d61-132">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f7d61-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f7d61-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7d61-133">NOTES</span></span>

## <span data-ttu-id="f7d61-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7d61-134">RELATED LINKS</span></span>
