---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503876"
---
# <span data-ttu-id="b671c-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="b671c-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="b671c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b671c-102">SYNOPSIS</span></span>
<span data-ttu-id="b671c-103">Pobiera CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="b671c-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="b671c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b671c-104">SYNTAX</span></span>

### <span data-ttu-id="b671c-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b671c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b671c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b671c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b671c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b671c-107">DESCRIPTION</span></span>
<span data-ttu-id="b671c-108">Polecenie cmdlet **Get-AzCosmosDBCassandraKeyspace** umożliwia utworzenie nowego lub zaktualizowanie istniejącego CosmosDB Cassandra miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="b671c-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="b671c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b671c-109">EXAMPLES</span></span>

### <span data-ttu-id="b671c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b671c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="b671c-111">Get-AzCosmosDBCassandraKeyspace pobiera właściwości istniejącego CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="b671c-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="b671c-112">Możesz rozwinąć zasób, aby uzyskać _etag, _ts _rid właściwości.</span><span class="sxs-lookup"><span data-stu-id="b671c-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="b671c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b671c-113">PARAMETERS</span></span>

### <span data-ttu-id="b671c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b671c-114">-AccountName</span></span>
<span data-ttu-id="b671c-115">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b671c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b671c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b671c-116">-DefaultProfile</span></span>
<span data-ttu-id="b671c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b671c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b671c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b671c-118">-Name</span></span>
<span data-ttu-id="b671c-119">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="b671c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b671c-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b671c-120">-ParentObject</span></span>
<span data-ttu-id="b671c-121">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b671c-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b671c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b671c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b671c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b671c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b671c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b671c-124">CommonParameters</span></span>
<span data-ttu-id="b671c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b671c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b671c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b671c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b671c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b671c-127">INPUTS</span></span>

### <span data-ttu-id="b671c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b671c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b671c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b671c-129">OUTPUTS</span></span>

### <span data-ttu-id="b671c-130">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b671c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="b671c-131">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b671c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b671c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b671c-132">NOTES</span></span>

## <span data-ttu-id="b671c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b671c-133">RELATED LINKS</span></span>
