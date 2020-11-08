---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221365"
---
# <span data-ttu-id="6e0a5-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="6e0a5-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="6e0a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0a5-103">Pobiera CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6e0a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e0a5-104">SYNTAX</span></span>

### <span data-ttu-id="6e0a5-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e0a5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e0a5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e0a5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e0a5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e0a5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e0a5-108">Polecenie cmdlet **Get-AzCosmosDBCassandraKeyspace** umożliwia utworzenie nowego lub zaktualizowanie istniejącego CosmosDB Cassandra miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6e0a5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e0a5-109">EXAMPLES</span></span>

### <span data-ttu-id="6e0a5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e0a5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="6e0a5-111">Get-AzCosmosDBCassandraKeyspace pobiera właściwości istniejącego CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="6e0a5-112">Możesz rozwinąć zasób, aby uzyskać _etag, _ts _rid właściwości.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="6e0a5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e0a5-113">PARAMETERS</span></span>

### <span data-ttu-id="6e0a5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e0a5-114">-AccountName</span></span>
<span data-ttu-id="6e0a5-115">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6e0a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0a5-116">-DefaultProfile</span></span>
<span data-ttu-id="6e0a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0a5-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e0a5-118">-Name</span></span>
<span data-ttu-id="6e0a5-119">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6e0a5-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6e0a5-120">-ParentObject</span></span>
<span data-ttu-id="6e0a5-121">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6e0a5-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6e0a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e0a5-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6e0a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0a5-124">CommonParameters</span></span>
<span data-ttu-id="6e0a5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0a5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e0a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0a5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e0a5-127">INPUTS</span></span>

### <span data-ttu-id="6e0a5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6e0a5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6e0a5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e0a5-129">OUTPUTS</span></span>

### <span data-ttu-id="6e0a5-130">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6e0a5-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="6e0a5-131">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6e0a5-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6e0a5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e0a5-132">NOTES</span></span>

## <span data-ttu-id="6e0a5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e0a5-133">RELATED LINKS</span></span>
