---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199067"
---
# <span data-ttu-id="6e0a2-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="6e0a2-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="6e0a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0a2-103">Pobiera cassandra Keyspace z bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6e0a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6e0a2-104">SYNTAX</span></span>

### <span data-ttu-id="6e0a2-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6e0a2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e0a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e0a2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e0a2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6e0a2-107">DESCRIPTION</span></span>
<span data-ttu-id="6e0a2-108">Polecenie **cmdlet Get-AzCosmosDBCassandraKeyspace** tworzy nową lub aktualizuje istniejącą spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6e0a2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6e0a2-109">EXAMPLES</span></span>

### <span data-ttu-id="6e0a2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e0a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="6e0a2-111">Get-AzCosmosDBCassandraKeyspace właściwości istniejącej cassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="6e0a2-112">Możesz rozwinąć zasób, aby uzyskać _etag, _ts _rid właściwości.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="6e0a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e0a2-113">PARAMETERS</span></span>

### <span data-ttu-id="6e0a2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e0a2-114">-AccountName</span></span>
<span data-ttu-id="6e0a2-115">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6e0a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0a2-116">-DefaultProfile</span></span>
<span data-ttu-id="6e0a2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0a2-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6e0a2-118">-Name</span></span>
<span data-ttu-id="6e0a2-119">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6e0a2-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="6e0a2-120">-ParentObject</span></span>
<span data-ttu-id="6e0a2-121">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="6e0a2-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6e0a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e0a2-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6e0a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0a2-124">CommonParameters</span></span>
<span data-ttu-id="6e0a2-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0a2-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e0a2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0a2-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e0a2-127">INPUTS</span></span>

### <span data-ttu-id="6e0a2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6e0a2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6e0a2-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e0a2-129">OUTPUTS</span></span>

### <span data-ttu-id="6e0a2-130">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6e0a2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="6e0a2-131">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6e0a2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6e0a2-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6e0a2-132">NOTES</span></span>

## <span data-ttu-id="6e0a2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e0a2-133">RELATED LINKS</span></span>
