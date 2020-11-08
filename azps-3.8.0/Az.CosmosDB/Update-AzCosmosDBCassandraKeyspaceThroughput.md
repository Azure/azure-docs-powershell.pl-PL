---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 0c104573fe0ecfb710f37c9c2fe898a6777f49e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049508"
---
# <span data-ttu-id="e8722-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="e8722-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="e8722-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8722-102">SYNOPSIS</span></span>
<span data-ttu-id="e8722-103">Aktualizuje wartość przepływności w CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e8722-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="e8722-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8722-104">SYNTAX</span></span>

### <span data-ttu-id="e8722-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8722-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8722-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8722-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8722-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8722-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8722-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8722-108">EXAMPLES</span></span>

### <span data-ttu-id="e8722-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8722-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e8722-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8722-110">PARAMETERS</span></span>

### <span data-ttu-id="e8722-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8722-111">-AccountName</span></span>
<span data-ttu-id="e8722-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8722-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8722-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8722-113">-Confirm</span></span>
<span data-ttu-id="e8722-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8722-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8722-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8722-115">-DefaultProfile</span></span>
<span data-ttu-id="e8722-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8722-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8722-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8722-117">-InputObject</span></span>
<span data-ttu-id="e8722-118">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e8722-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e8722-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8722-119">-Name</span></span>
<span data-ttu-id="e8722-120">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="e8722-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e8722-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e8722-121">-ParentObject</span></span>
<span data-ttu-id="e8722-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e8722-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e8722-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8722-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8722-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8722-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e8722-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="e8722-125">-Throughput</span></span>
<span data-ttu-id="e8722-126">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e8722-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e8722-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="e8722-127">Default value is 400.</span></span>

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

### <span data-ttu-id="e8722-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8722-128">-WhatIf</span></span>
<span data-ttu-id="e8722-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8722-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8722-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8722-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8722-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8722-131">CommonParameters</span></span>
<span data-ttu-id="e8722-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8722-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8722-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8722-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8722-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8722-134">INPUTS</span></span>

### <span data-ttu-id="e8722-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e8722-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e8722-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8722-136">OUTPUTS</span></span>

### <span data-ttu-id="e8722-137">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e8722-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e8722-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8722-138">NOTES</span></span>

## <span data-ttu-id="e8722-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8722-139">RELATED LINKS</span></span>
