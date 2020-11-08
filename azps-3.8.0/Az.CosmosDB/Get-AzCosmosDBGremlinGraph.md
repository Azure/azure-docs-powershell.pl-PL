---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053088"
---
# <span data-ttu-id="0c1dc-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="0c1dc-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="0c1dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1dc-103">Pobiera wykres Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0c1dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c1dc-104">SYNTAX</span></span>

### <span data-ttu-id="0c1dc-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c1dc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="0c1dc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c1dc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c1dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c1dc-107">DESCRIPTION</span></span>
<span data-ttu-id="0c1dc-108">Polecenie cmdlet **Get-AzCosmosDBGremlinGraph** pobiera właściwości CosmosDB Gremlin wykresu.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="0c1dc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c1dc-109">EXAMPLES</span></span>

### <span data-ttu-id="0c1dc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c1dc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="0c1dc-111">Obiekt zasobu zawiera IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="0c1dc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c1dc-112">PARAMETERS</span></span>

### <span data-ttu-id="0c1dc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c1dc-113">-AccountName</span></span>
<span data-ttu-id="0c1dc-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c1dc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c1dc-115">-DatabaseName</span></span>
<span data-ttu-id="0c1dc-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-116">Database name.</span></span>

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

### <span data-ttu-id="0c1dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1dc-117">-DefaultProfile</span></span>
<span data-ttu-id="0c1dc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c1dc-119">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="0c1dc-119">-Detailed</span></span>
<span data-ttu-id="0c1dc-120">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci wykres Gremlin z odpowiednią wartością przepływności.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="0c1dc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c1dc-121">-InputObject</span></span>
<span data-ttu-id="0c1dc-122">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="0c1dc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c1dc-123">-Name</span></span>
<span data-ttu-id="0c1dc-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0c1dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c1dc-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-126">Name of resource group.</span></span>

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

### <span data-ttu-id="0c1dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1dc-127">CommonParameters</span></span>
<span data-ttu-id="0c1dc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c1dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1dc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c1dc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1dc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c1dc-130">INPUTS</span></span>

### <span data-ttu-id="0c1dc-131">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0c1dc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="0c1dc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c1dc-132">OUTPUTS</span></span>

### <span data-ttu-id="0c1dc-133">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="0c1dc-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="0c1dc-134">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0c1dc-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0c1dc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c1dc-135">NOTES</span></span>

## <span data-ttu-id="0c1dc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c1dc-136">RELATED LINKS</span></span>
