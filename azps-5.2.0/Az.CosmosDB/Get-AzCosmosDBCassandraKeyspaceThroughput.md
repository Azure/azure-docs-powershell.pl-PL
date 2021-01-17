---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367297"
---
# <span data-ttu-id="f7d3b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="f7d3b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="f7d3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d3b-103">Pobiera wartość przepływności dla obszaru Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="f7d3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7d3b-104">SYNTAX</span></span>

### <span data-ttu-id="f7d3b-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7d3b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d3b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7d3b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d3b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7d3b-107">DESCRIPTION</span></span>
<span data-ttu-id="f7d3b-108">Polecenie cmdlet **Get-AzCosmosDBCassandraKeyspaceThroughput** pobiera obiekt przepływności odpowiadający danej przestrzeni.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="f7d3b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7d3b-109">EXAMPLES</span></span>

### <span data-ttu-id="f7d3b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7d3b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="f7d3b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7d3b-111">PARAMETERS</span></span>

### <span data-ttu-id="f7d3b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7d3b-112">-AccountName</span></span>
<span data-ttu-id="f7d3b-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7d3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d3b-114">-DefaultProfile</span></span>
<span data-ttu-id="f7d3b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d3b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7d3b-116">-InputObject</span></span>
<span data-ttu-id="f7d3b-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f7d3b-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f7d3b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7d3b-118">-Name</span></span>
<span data-ttu-id="f7d3b-119">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7d3b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f7d3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d3b-122">CommonParameters</span></span>
<span data-ttu-id="f7d3b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d3b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d3b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d3b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7d3b-125">INPUTS</span></span>

### <span data-ttu-id="f7d3b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f7d3b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f7d3b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7d3b-127">OUTPUTS</span></span>

### <span data-ttu-id="f7d3b-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f7d3b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f7d3b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7d3b-129">NOTES</span></span>

## <span data-ttu-id="f7d3b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7d3b-130">RELATED LINKS</span></span>
