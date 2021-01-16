---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344650"
---
# <span data-ttu-id="39823-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="39823-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="39823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39823-102">SYNOPSIS</span></span>
<span data-ttu-id="39823-103">Aktualizuje wartość przepływności w CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39823-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="39823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39823-104">SYNTAX</span></span>

### <span data-ttu-id="39823-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39823-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39823-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39823-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39823-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39823-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39823-108">Opis</span><span class="sxs-lookup"><span data-stu-id="39823-108">DESCRIPTION</span></span>
<span data-ttu-id="39823-109">Aktualizuje wartość przepływności w CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39823-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="39823-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39823-110">EXAMPLES</span></span>

### <span data-ttu-id="39823-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39823-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="39823-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39823-112">PARAMETERS</span></span>

### <span data-ttu-id="39823-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39823-113">-AccountName</span></span>
<span data-ttu-id="39823-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="39823-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39823-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="39823-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="39823-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="39823-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39823-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39823-117">-Confirm</span></span>
<span data-ttu-id="39823-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39823-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39823-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39823-119">-DefaultProfile</span></span>
<span data-ttu-id="39823-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39823-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39823-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39823-121">-InputObject</span></span>
<span data-ttu-id="39823-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39823-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39823-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39823-123">-Name</span></span>
<span data-ttu-id="39823-124">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="39823-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="39823-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="39823-125">-ParentObject</span></span>
<span data-ttu-id="39823-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39823-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="39823-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39823-127">-ResourceGroupName</span></span>
<span data-ttu-id="39823-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39823-128">Name of resource group.</span></span>

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

### <span data-ttu-id="39823-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="39823-129">-Throughput</span></span>
<span data-ttu-id="39823-130">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="39823-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="39823-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="39823-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39823-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39823-132">-WhatIf</span></span>
<span data-ttu-id="39823-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39823-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39823-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39823-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39823-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39823-135">CommonParameters</span></span>
<span data-ttu-id="39823-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39823-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39823-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39823-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39823-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39823-138">INPUTS</span></span>

### <span data-ttu-id="39823-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="39823-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="39823-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39823-140">OUTPUTS</span></span>

### <span data-ttu-id="39823-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="39823-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="39823-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39823-142">NOTES</span></span>

## <span data-ttu-id="39823-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39823-143">RELATED LINKS</span></span>
