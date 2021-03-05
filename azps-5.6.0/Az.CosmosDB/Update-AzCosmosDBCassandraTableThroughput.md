---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 989035c1478228eb8895a2f99779129c605b2f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977418"
---
# <span data-ttu-id="1289d-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="1289d-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="1289d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1289d-102">SYNOPSIS</span></span>
<span data-ttu-id="1289d-103">Aktualizuje wartość przepływności tabeli Cassandradrydydy.</span><span class="sxs-lookup"><span data-stu-id="1289d-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="1289d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1289d-104">SYNTAX</span></span>

### <span data-ttu-id="1289d-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1289d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1289d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1289d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1289d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1289d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1289d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1289d-108">DESCRIPTION</span></span>
<span data-ttu-id="1289d-109">Aktualizuje wartość przepływności tabeli Cassandradrydydy.</span><span class="sxs-lookup"><span data-stu-id="1289d-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="1289d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1289d-110">EXAMPLES</span></span>

### <span data-ttu-id="1289d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1289d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="1289d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1289d-112">PARAMETERS</span></span>

### <span data-ttu-id="1289d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1289d-113">-AccountName</span></span>
<span data-ttu-id="1289d-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="1289d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1289d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1289d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1289d-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="1289d-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1289d-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1289d-117">-Confirm</span></span>
<span data-ttu-id="1289d-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1289d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1289d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1289d-119">-DefaultProfile</span></span>
<span data-ttu-id="1289d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1289d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1289d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1289d-121">-InputObject</span></span>
<span data-ttu-id="1289d-122">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1289d-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1289d-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="1289d-123">-KeyspaceName</span></span>
<span data-ttu-id="1289d-124">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1289d-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1289d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1289d-125">-Name</span></span>
<span data-ttu-id="1289d-126">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1289d-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="1289d-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="1289d-127">-ParentObject</span></span>
<span data-ttu-id="1289d-128">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1289d-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1289d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1289d-129">-ResourceGroupName</span></span>
<span data-ttu-id="1289d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1289d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="1289d-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="1289d-131">-Throughput</span></span>
<span data-ttu-id="1289d-132">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1289d-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1289d-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="1289d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="1289d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1289d-134">-WhatIf</span></span>
<span data-ttu-id="1289d-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1289d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1289d-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1289d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1289d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1289d-137">CommonParameters</span></span>
<span data-ttu-id="1289d-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1289d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1289d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1289d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1289d-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1289d-140">INPUTS</span></span>

### <span data-ttu-id="1289d-141">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1289d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1289d-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1289d-142">OUTPUTS</span></span>

### <span data-ttu-id="1289d-143">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1289d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1289d-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1289d-144">NOTES</span></span>

## <span data-ttu-id="1289d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1289d-145">RELATED LINKS</span></span>
