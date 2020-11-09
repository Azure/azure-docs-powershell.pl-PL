---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307320"
---
# <span data-ttu-id="fd92b-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="fd92b-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="fd92b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd92b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd92b-103">Pobiera tabelę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="fd92b-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="fd92b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd92b-104">SYNTAX</span></span>

### <span data-ttu-id="fd92b-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd92b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd92b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd92b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd92b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd92b-107">DESCRIPTION</span></span>
<span data-ttu-id="fd92b-108">Polecenie cmdlet **Get-AzCosmosDBCassandraTable** umożliwia utworzenie nowego lub zaktualizowanie istniejącego CosmosDB Cassandra miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="fd92b-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="fd92b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd92b-109">EXAMPLES</span></span>

### <span data-ttu-id="fd92b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd92b-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="fd92b-111">{{Get-AzCosmosDBCassandraTable pobiera właściwości istniejącego CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="fd92b-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="fd92b-112">Możesz rozwinąć zasób, aby pobrać właściwości DefaultTtl, Schema, _etag, _ts _rid.}}</span><span class="sxs-lookup"><span data-stu-id="fd92b-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="fd92b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd92b-113">PARAMETERS</span></span>

### <span data-ttu-id="fd92b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd92b-114">-AccountName</span></span>
<span data-ttu-id="fd92b-115">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="fd92b-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fd92b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd92b-116">-DefaultProfile</span></span>
<span data-ttu-id="fd92b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd92b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd92b-118">-Spacename</span><span class="sxs-lookup"><span data-stu-id="fd92b-118">-KeyspaceName</span></span>
<span data-ttu-id="fd92b-119">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="fd92b-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="fd92b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd92b-120">-Name</span></span>
<span data-ttu-id="fd92b-121">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fd92b-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="fd92b-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="fd92b-122">-ParentObject</span></span>
<span data-ttu-id="fd92b-123">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="fd92b-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="fd92b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd92b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd92b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd92b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="fd92b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd92b-126">CommonParameters</span></span>
<span data-ttu-id="fd92b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd92b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd92b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd92b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd92b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd92b-129">INPUTS</span></span>

### <span data-ttu-id="fd92b-130">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="fd92b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="fd92b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd92b-131">OUTPUTS</span></span>

### <span data-ttu-id="fd92b-132">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fd92b-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="fd92b-133">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fd92b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fd92b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd92b-134">NOTES</span></span>

## <span data-ttu-id="fd92b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd92b-135">RELATED LINKS</span></span>
