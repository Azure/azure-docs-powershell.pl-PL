---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053389"
---
# <span data-ttu-id="b7015-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="b7015-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="b7015-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7015-102">SYNOPSIS</span></span>
<span data-ttu-id="b7015-103">Umożliwia zaktualizowanie wartości przepływności tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b7015-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="b7015-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7015-104">SYNTAX</span></span>

### <span data-ttu-id="b7015-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7015-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7015-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7015-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7015-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7015-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7015-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7015-108">EXAMPLES</span></span>

### <span data-ttu-id="b7015-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7015-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="b7015-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7015-110">PARAMETERS</span></span>

### <span data-ttu-id="b7015-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7015-111">-AccountName</span></span>
<span data-ttu-id="b7015-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b7015-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b7015-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7015-113">-Confirm</span></span>
<span data-ttu-id="b7015-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7015-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7015-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7015-115">-DefaultProfile</span></span>
<span data-ttu-id="b7015-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7015-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7015-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7015-117">-InputObject</span></span>
<span data-ttu-id="b7015-118">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="b7015-118">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b7015-119">-Spacename</span><span class="sxs-lookup"><span data-stu-id="b7015-119">-KeyspaceName</span></span>
<span data-ttu-id="b7015-120">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="b7015-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b7015-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7015-121">-Name</span></span>
<span data-ttu-id="b7015-122">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="b7015-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="b7015-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b7015-123">-ParentObject</span></span>
<span data-ttu-id="b7015-124">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="b7015-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b7015-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7015-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7015-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7015-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b7015-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="b7015-127">-Throughput</span></span>
<span data-ttu-id="b7015-128">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b7015-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="b7015-129">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="b7015-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7015-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7015-130">-WhatIf</span></span>
<span data-ttu-id="b7015-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7015-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7015-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7015-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7015-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7015-133">CommonParameters</span></span>
<span data-ttu-id="b7015-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7015-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7015-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7015-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7015-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7015-136">INPUTS</span></span>

### <span data-ttu-id="b7015-137">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b7015-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="b7015-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7015-138">OUTPUTS</span></span>

### <span data-ttu-id="b7015-139">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b7015-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b7015-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7015-140">NOTES</span></span>

## <span data-ttu-id="b7015-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7015-141">RELATED LINKS</span></span>
