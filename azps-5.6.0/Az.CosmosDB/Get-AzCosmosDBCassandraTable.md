---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 2d784a82974f47c67bae89d55042b81c9c83e273
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978737"
---
# <span data-ttu-id="66293-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="66293-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="66293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66293-102">SYNOPSIS</span></span>
<span data-ttu-id="66293-103">Pobiera tabelę CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="66293-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="66293-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66293-104">SYNTAX</span></span>

### <span data-ttu-id="66293-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="66293-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66293-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66293-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66293-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="66293-107">DESCRIPTION</span></span>
<span data-ttu-id="66293-108">Polecenie **cmdlet Get-AzCosmosDBCassandraTable** tworzy nową lub aktualizuje istniejącą spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="66293-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="66293-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66293-109">EXAMPLES</span></span>

### <span data-ttu-id="66293-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66293-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="66293-111">{{ Get-AzCosmosDBCassandraTable pobiera właściwości istniejącej cassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="66293-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="66293-112">Możesz rozwinąć zasób, aby uzyskać właściwości DefaultTtl, Schema, _etag, _ts _rid}}}</span><span class="sxs-lookup"><span data-stu-id="66293-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="66293-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66293-113">PARAMETERS</span></span>

### <span data-ttu-id="66293-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66293-114">-AccountName</span></span>
<span data-ttu-id="66293-115">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="66293-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66293-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66293-116">-DefaultProfile</span></span>
<span data-ttu-id="66293-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66293-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66293-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="66293-118">-KeyspaceName</span></span>
<span data-ttu-id="66293-119">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66293-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="66293-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66293-120">-Name</span></span>
<span data-ttu-id="66293-121">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66293-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="66293-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="66293-122">-ParentObject</span></span>
<span data-ttu-id="66293-123">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="66293-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66293-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66293-124">-ResourceGroupName</span></span>
<span data-ttu-id="66293-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66293-125">Name of resource group.</span></span>

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

### <span data-ttu-id="66293-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66293-126">CommonParameters</span></span>
<span data-ttu-id="66293-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66293-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66293-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66293-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66293-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66293-129">INPUTS</span></span>

### <span data-ttu-id="66293-130">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="66293-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="66293-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66293-131">OUTPUTS</span></span>

### <span data-ttu-id="66293-132">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="66293-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="66293-133">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="66293-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="66293-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66293-134">NOTES</span></span>

## <span data-ttu-id="66293-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66293-135">RELATED LINKS</span></span>
