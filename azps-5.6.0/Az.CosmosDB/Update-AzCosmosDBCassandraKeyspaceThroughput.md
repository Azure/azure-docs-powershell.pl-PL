---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 34401fb2e6b18e2b4f68e15eb004e440f99a3858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977441"
---
# <span data-ttu-id="80c61-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="80c61-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="80c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c61-102">SYNOPSIS</span></span>
<span data-ttu-id="80c61-103">Aktualizuje wartość przepływności dla cassandra keyspacedrydadb.</span><span class="sxs-lookup"><span data-stu-id="80c61-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="80c61-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80c61-104">SYNTAX</span></span>

### <span data-ttu-id="80c61-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="80c61-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c61-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80c61-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c61-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80c61-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c61-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="80c61-108">DESCRIPTION</span></span>
<span data-ttu-id="80c61-109">Aktualizuje wartość przepływności dla cassandra keyspacedrydadb.</span><span class="sxs-lookup"><span data-stu-id="80c61-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="80c61-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80c61-110">EXAMPLES</span></span>

### <span data-ttu-id="80c61-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80c61-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="80c61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c61-112">PARAMETERS</span></span>

### <span data-ttu-id="80c61-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80c61-113">-AccountName</span></span>
<span data-ttu-id="80c61-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="80c61-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="80c61-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="80c61-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="80c61-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="80c61-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="80c61-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80c61-117">-Confirm</span></span>
<span data-ttu-id="80c61-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80c61-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c61-119">-DefaultProfile</span></span>
<span data-ttu-id="80c61-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80c61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c61-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c61-121">-InputObject</span></span>
<span data-ttu-id="80c61-122">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="80c61-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="80c61-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80c61-123">-Name</span></span>
<span data-ttu-id="80c61-124">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="80c61-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="80c61-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="80c61-125">-ParentObject</span></span>
<span data-ttu-id="80c61-126">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="80c61-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="80c61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c61-127">-ResourceGroupName</span></span>
<span data-ttu-id="80c61-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80c61-128">Name of resource group.</span></span>

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

### <span data-ttu-id="80c61-129">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="80c61-129">-Throughput</span></span>
<span data-ttu-id="80c61-130">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="80c61-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="80c61-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="80c61-131">Default value is 400.</span></span>

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

### <span data-ttu-id="80c61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c61-132">-WhatIf</span></span>
<span data-ttu-id="80c61-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c61-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80c61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c61-135">CommonParameters</span></span>
<span data-ttu-id="80c61-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c61-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c61-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c61-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80c61-138">INPUTS</span></span>

### <span data-ttu-id="80c61-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="80c61-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="80c61-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80c61-140">OUTPUTS</span></span>

### <span data-ttu-id="80c61-141">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="80c61-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="80c61-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80c61-142">NOTES</span></span>

## <span data-ttu-id="80c61-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80c61-143">RELATED LINKS</span></span>
