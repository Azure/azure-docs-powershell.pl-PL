---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503839"
---
# <span data-ttu-id="46061-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="46061-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="46061-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46061-102">SYNOPSIS</span></span>
<span data-ttu-id="46061-103">Tworzy nową tabelę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="46061-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="46061-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46061-104">SYNTAX</span></span>

### <span data-ttu-id="46061-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46061-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46061-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46061-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46061-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46061-107">DESCRIPTION</span></span>
<span data-ttu-id="46061-108">Tworzy nową tabelę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="46061-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="46061-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46061-109">EXAMPLES</span></span>

### <span data-ttu-id="46061-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46061-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="46061-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46061-111">PARAMETERS</span></span>

### <span data-ttu-id="46061-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46061-112">-AccountName</span></span>
<span data-ttu-id="46061-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="46061-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46061-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="46061-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="46061-115">Czas wygaśnięcia magazynu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="46061-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="46061-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="46061-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="46061-117">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="46061-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="46061-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46061-118">-Confirm</span></span>
<span data-ttu-id="46061-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46061-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46061-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46061-120">-DefaultProfile</span></span>
<span data-ttu-id="46061-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46061-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46061-122">-Spacename</span><span class="sxs-lookup"><span data-stu-id="46061-122">-KeyspaceName</span></span>
<span data-ttu-id="46061-123">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="46061-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="46061-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46061-124">-Name</span></span>
<span data-ttu-id="46061-125">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="46061-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="46061-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="46061-126">-ParentObject</span></span>
<span data-ttu-id="46061-127">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="46061-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="46061-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46061-128">-ResourceGroupName</span></span>
<span data-ttu-id="46061-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46061-129">Name of resource group.</span></span>

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

### <span data-ttu-id="46061-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="46061-130">-Schema</span></span>
<span data-ttu-id="46061-131">Obiekt PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="46061-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="46061-132">Użyj New-AzCosmosDBCassandraSchema, aby utworzyć ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="46061-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46061-133">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="46061-133">-Throughput</span></span>
<span data-ttu-id="46061-134">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="46061-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="46061-135">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="46061-135">Default value is 400.</span></span>

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

### <span data-ttu-id="46061-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="46061-136">-TtlInSeconds</span></span>
<span data-ttu-id="46061-137">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="46061-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="46061-138">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="46061-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="46061-139">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="46061-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="46061-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46061-140">-WhatIf</span></span>
<span data-ttu-id="46061-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46061-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46061-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46061-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46061-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46061-143">CommonParameters</span></span>
<span data-ttu-id="46061-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46061-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46061-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46061-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46061-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46061-146">INPUTS</span></span>

### <span data-ttu-id="46061-147">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="46061-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="46061-148">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="46061-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="46061-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46061-149">OUTPUTS</span></span>

### <span data-ttu-id="46061-150">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="46061-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="46061-151">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="46061-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="46061-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46061-152">NOTES</span></span>

## <span data-ttu-id="46061-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46061-153">RELATED LINKS</span></span>
