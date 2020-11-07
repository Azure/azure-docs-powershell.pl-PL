---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894794"
---
# <span data-ttu-id="11062-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="11062-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="11062-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11062-102">SYNOPSIS</span></span>
<span data-ttu-id="11062-103">Pobiera CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="11062-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="11062-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11062-104">SYNTAX</span></span>

### <span data-ttu-id="11062-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11062-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11062-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11062-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11062-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11062-107">DESCRIPTION</span></span>
<span data-ttu-id="11062-108">Polecenie cmdlet **Get-AzCosmosDBCassandraKeyspace** umożliwia utworzenie nowego lub zaktualizowanie istniejącego CosmosDB Cassandra miejsca na dysku.</span><span class="sxs-lookup"><span data-stu-id="11062-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="11062-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11062-109">EXAMPLES</span></span>

### <span data-ttu-id="11062-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11062-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="11062-111">Get-AzCosmosDBCassandraKeyspace pobiera właściwości istniejącego CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="11062-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="11062-112">Możesz rozwinąć zasób, aby uzyskać _etag, _ts _rid właściwości.</span><span class="sxs-lookup"><span data-stu-id="11062-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="11062-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11062-113">PARAMETERS</span></span>

### <span data-ttu-id="11062-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11062-114">-AccountName</span></span>
<span data-ttu-id="11062-115">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="11062-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11062-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11062-116">-DefaultProfile</span></span>
<span data-ttu-id="11062-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11062-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11062-118">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="11062-118">-Detailed</span></span>
<span data-ttu-id="11062-119">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci wartość określającą ilość miejsca w odpowiedniej wartości przepustowości.</span><span class="sxs-lookup"><span data-stu-id="11062-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="11062-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11062-120">-InputObject</span></span>
<span data-ttu-id="11062-121">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="11062-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11062-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11062-122">-Name</span></span>
<span data-ttu-id="11062-123">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="11062-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="11062-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11062-124">-ResourceGroupName</span></span>
<span data-ttu-id="11062-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11062-125">Name of resource group.</span></span>

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

### <span data-ttu-id="11062-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11062-126">CommonParameters</span></span>
<span data-ttu-id="11062-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11062-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11062-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11062-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11062-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11062-129">INPUTS</span></span>

### <span data-ttu-id="11062-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="11062-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="11062-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11062-131">OUTPUTS</span></span>

### <span data-ttu-id="11062-132">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="11062-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="11062-133">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="11062-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="11062-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11062-134">NOTES</span></span>

## <span data-ttu-id="11062-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11062-135">RELATED LINKS</span></span>
