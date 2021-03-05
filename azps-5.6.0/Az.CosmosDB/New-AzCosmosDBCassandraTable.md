---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7251b4b928bb0adc94bc42da9d5bcef063c86259
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008001"
---
# <span data-ttu-id="7fc3a-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="7fc3a-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="7fc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc3a-103">Tworzy nową tabelę CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="7fc3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7fc3a-104">SYNTAX</span></span>

### <span data-ttu-id="7fc3a-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7fc3a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc3a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fc3a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fc3a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7fc3a-107">DESCRIPTION</span></span>
<span data-ttu-id="7fc3a-108">Tworzy nową tabelę CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="7fc3a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7fc3a-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc3a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fc3a-110">Example 1</span></span>
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

## <span data-ttu-id="7fc3a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fc3a-111">PARAMETERS</span></span>

### <span data-ttu-id="7fc3a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fc3a-112">-AccountName</span></span>
<span data-ttu-id="7fc3a-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fc3a-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="7fc3a-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="7fc3a-115">TTL (Czas wygaśnięcia magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="7fc3a-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="7fc3a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7fc3a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7fc3a-117">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7fc3a-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fc3a-118">-Confirm</span></span>
<span data-ttu-id="7fc3a-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc3a-120">-DefaultProfile</span></span>
<span data-ttu-id="7fc3a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc3a-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="7fc3a-122">-KeyspaceName</span></span>
<span data-ttu-id="7fc3a-123">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7fc3a-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7fc3a-124">-Name</span></span>
<span data-ttu-id="7fc3a-125">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="7fc3a-126">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="7fc3a-126">-ParentObject</span></span>
<span data-ttu-id="7fc3a-127">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="7fc3a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc3a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fc3a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="7fc3a-130">— Schemat</span><span class="sxs-lookup"><span data-stu-id="7fc3a-130">-Schema</span></span>
<span data-ttu-id="7fc3a-131">Obiekt PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="7fc3a-132">Użyj New-AzCosmosDBCassandraSchema, aby utworzyć ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="7fc3a-133">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="7fc3a-133">-Throughput</span></span>
<span data-ttu-id="7fc3a-134">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7fc3a-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="7fc3a-135">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-135">Default value is 400.</span></span>

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

### <span data-ttu-id="7fc3a-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="7fc3a-136">-TtlInSeconds</span></span>
<span data-ttu-id="7fc3a-137">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="7fc3a-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="7fc3a-138">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="7fc3a-139">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="7fc3a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc3a-140">-WhatIf</span></span>
<span data-ttu-id="7fc3a-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc3a-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc3a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc3a-143">CommonParameters</span></span>
<span data-ttu-id="7fc3a-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc3a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc3a-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fc3a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc3a-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fc3a-146">INPUTS</span></span>

### <span data-ttu-id="7fc3a-147">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="7fc3a-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="7fc3a-148">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7fc3a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7fc3a-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fc3a-149">OUTPUTS</span></span>

### <span data-ttu-id="7fc3a-150">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="7fc3a-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="7fc3a-151">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7fc3a-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7fc3a-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7fc3a-152">NOTES</span></span>

## <span data-ttu-id="7fc3a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fc3a-153">RELATED LINKS</span></span>
