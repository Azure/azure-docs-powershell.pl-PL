---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983626"
---
# <span data-ttu-id="ff59d-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="ff59d-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="ff59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff59d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff59d-103">Pobiera wykres GrysDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="ff59d-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ff59d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff59d-104">SYNTAX</span></span>

### <span data-ttu-id="ff59d-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff59d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="ff59d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff59d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff59d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff59d-107">DESCRIPTION</span></span>
<span data-ttu-id="ff59d-108">Polecenie **cmdlet Get-AzCosmosDBGremlinGraph** pobiera właściwości GrysDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="ff59d-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="ff59d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff59d-109">EXAMPLES</span></span>

### <span data-ttu-id="ff59d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff59d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="ff59d-111">Obiekt zasobu zawiera właściwości IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="ff59d-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="ff59d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff59d-112">PARAMETERS</span></span>

### <span data-ttu-id="ff59d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff59d-113">-AccountName</span></span>
<span data-ttu-id="ff59d-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="ff59d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ff59d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff59d-115">-DatabaseName</span></span>
<span data-ttu-id="ff59d-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ff59d-116">Database name.</span></span>

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

### <span data-ttu-id="ff59d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff59d-117">-DefaultProfile</span></span>
<span data-ttu-id="ff59d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff59d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff59d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff59d-119">-Name</span></span>
<span data-ttu-id="ff59d-120">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ff59d-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="ff59d-121">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff59d-121">-ParentObject</span></span>
<span data-ttu-id="ff59d-122">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ff59d-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ff59d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff59d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff59d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff59d-124">Name of resource group.</span></span>

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

### <span data-ttu-id="ff59d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff59d-125">CommonParameters</span></span>
<span data-ttu-id="ff59d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff59d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff59d-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff59d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff59d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff59d-128">INPUTS</span></span>

### <span data-ttu-id="ff59d-129">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ff59d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="ff59d-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff59d-130">OUTPUTS</span></span>

### <span data-ttu-id="ff59d-131">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="ff59d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="ff59d-132">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ff59d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ff59d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff59d-133">NOTES</span></span>

## <span data-ttu-id="ff59d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff59d-134">RELATED LINKS</span></span>
