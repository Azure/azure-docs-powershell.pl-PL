---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978746"
---
# <span data-ttu-id="48ad9-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="48ad9-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="48ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="48ad9-103">Pobiera cassandra Keyspace z bazy danych Dosdb.</span><span class="sxs-lookup"><span data-stu-id="48ad9-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="48ad9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48ad9-104">SYNTAX</span></span>

### <span data-ttu-id="48ad9-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="48ad9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48ad9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ad9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ad9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="48ad9-107">DESCRIPTION</span></span>
<span data-ttu-id="48ad9-108">Polecenie **cmdlet Get-AzCosmosDBCassandraKeyspace** tworzy nową lub aktualizuje istniejącą spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="48ad9-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="48ad9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48ad9-109">EXAMPLES</span></span>

### <span data-ttu-id="48ad9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48ad9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="48ad9-111">Get-AzCosmosDBCassandraKeyspace właściwości istniejącej cassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="48ad9-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="48ad9-112">Możesz rozwinąć zasób, aby uzyskać _etag, _ts, _rid właściwości.</span><span class="sxs-lookup"><span data-stu-id="48ad9-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="48ad9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48ad9-113">PARAMETERS</span></span>

### <span data-ttu-id="48ad9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48ad9-114">-AccountName</span></span>
<span data-ttu-id="48ad9-115">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="48ad9-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="48ad9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ad9-116">-DefaultProfile</span></span>
<span data-ttu-id="48ad9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48ad9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ad9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48ad9-118">-Name</span></span>
<span data-ttu-id="48ad9-119">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="48ad9-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="48ad9-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="48ad9-120">-ParentObject</span></span>
<span data-ttu-id="48ad9-121">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="48ad9-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48ad9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ad9-122">-ResourceGroupName</span></span>
<span data-ttu-id="48ad9-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ad9-123">Name of resource group.</span></span>

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

### <span data-ttu-id="48ad9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ad9-124">CommonParameters</span></span>
<span data-ttu-id="48ad9-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ad9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ad9-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48ad9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ad9-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ad9-127">INPUTS</span></span>

### <span data-ttu-id="48ad9-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="48ad9-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="48ad9-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ad9-129">OUTPUTS</span></span>

### <span data-ttu-id="48ad9-130">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="48ad9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="48ad9-131">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="48ad9-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="48ad9-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48ad9-132">NOTES</span></span>

## <span data-ttu-id="48ad9-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48ad9-133">RELATED LINKS</span></span>
