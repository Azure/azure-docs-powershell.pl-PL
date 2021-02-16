---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199066"
---
# <span data-ttu-id="36b84-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="36b84-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="36b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b84-102">SYNOPSIS</span></span>
<span data-ttu-id="36b84-103">Pobiera wartość przepływności klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="36b84-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="36b84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36b84-104">SYNTAX</span></span>

### <span data-ttu-id="36b84-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="36b84-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36b84-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b84-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b84-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="36b84-107">DESCRIPTION</span></span>
<span data-ttu-id="36b84-108">Polecenie **cmdlet Get-AzCosmosDBCassandraKeyspaceThroughput** pobiera obiekt przepływności odpowiadający podanej klawiszowi Keyspace.</span><span class="sxs-lookup"><span data-stu-id="36b84-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="36b84-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36b84-109">EXAMPLES</span></span>

### <span data-ttu-id="36b84-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36b84-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="36b84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b84-111">PARAMETERS</span></span>

### <span data-ttu-id="36b84-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36b84-112">-AccountName</span></span>
<span data-ttu-id="36b84-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="36b84-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36b84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b84-114">-DefaultProfile</span></span>
<span data-ttu-id="36b84-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36b84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b84-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b84-116">-InputObject</span></span>
<span data-ttu-id="36b84-117">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="36b84-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="36b84-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36b84-118">-Name</span></span>
<span data-ttu-id="36b84-119">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="36b84-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="36b84-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b84-120">-ResourceGroupName</span></span>
<span data-ttu-id="36b84-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36b84-121">Name of resource group.</span></span>

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

### <span data-ttu-id="36b84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b84-122">CommonParameters</span></span>
<span data-ttu-id="36b84-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b84-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b84-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b84-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36b84-125">INPUTS</span></span>

### <span data-ttu-id="36b84-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="36b84-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="36b84-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36b84-127">OUTPUTS</span></span>

### <span data-ttu-id="36b84-128">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="36b84-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="36b84-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36b84-129">NOTES</span></span>

## <span data-ttu-id="36b84-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36b84-130">RELATED LINKS</span></span>
