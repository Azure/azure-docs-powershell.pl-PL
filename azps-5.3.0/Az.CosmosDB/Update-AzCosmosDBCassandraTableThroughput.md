---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501697"
---
# <span data-ttu-id="42641-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="42641-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="42641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42641-102">SYNOPSIS</span></span>
<span data-ttu-id="42641-103">Umożliwia zaktualizowanie wartości przepływności tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="42641-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="42641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42641-104">SYNTAX</span></span>

### <span data-ttu-id="42641-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42641-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42641-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42641-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42641-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42641-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42641-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42641-108">DESCRIPTION</span></span>
<span data-ttu-id="42641-109">Umożliwia zaktualizowanie wartości przepływności tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="42641-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="42641-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42641-110">EXAMPLES</span></span>

### <span data-ttu-id="42641-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42641-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="42641-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42641-112">PARAMETERS</span></span>

### <span data-ttu-id="42641-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42641-113">-AccountName</span></span>
<span data-ttu-id="42641-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="42641-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42641-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="42641-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="42641-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="42641-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="42641-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42641-117">-Confirm</span></span>
<span data-ttu-id="42641-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42641-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42641-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42641-119">-DefaultProfile</span></span>
<span data-ttu-id="42641-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42641-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42641-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42641-121">-InputObject</span></span>
<span data-ttu-id="42641-122">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="42641-122">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42641-123">-Spacename</span><span class="sxs-lookup"><span data-stu-id="42641-123">-KeyspaceName</span></span>
<span data-ttu-id="42641-124">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="42641-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="42641-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42641-125">-Name</span></span>
<span data-ttu-id="42641-126">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="42641-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="42641-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="42641-127">-ParentObject</span></span>
<span data-ttu-id="42641-128">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="42641-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="42641-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42641-129">-ResourceGroupName</span></span>
<span data-ttu-id="42641-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42641-130">Name of resource group.</span></span>

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

### <span data-ttu-id="42641-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="42641-131">-Throughput</span></span>
<span data-ttu-id="42641-132">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="42641-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="42641-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="42641-133">Default value is 400.</span></span>

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

### <span data-ttu-id="42641-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42641-134">-WhatIf</span></span>
<span data-ttu-id="42641-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42641-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42641-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42641-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42641-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42641-137">CommonParameters</span></span>
<span data-ttu-id="42641-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42641-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42641-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42641-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42641-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42641-140">INPUTS</span></span>

### <span data-ttu-id="42641-141">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="42641-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="42641-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42641-142">OUTPUTS</span></span>

### <span data-ttu-id="42641-143">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="42641-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="42641-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42641-144">NOTES</span></span>

## <span data-ttu-id="42641-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42641-145">RELATED LINKS</span></span>
