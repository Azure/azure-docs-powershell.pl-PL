---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 3f41c44c6abffaf5147ffba17fe3ec84561315b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977425"
---
# <span data-ttu-id="94e5c-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="94e5c-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="94e5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="94e5c-103">Aktualizuje tabelę Cassandrydy z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94e5c-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="94e5c-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="94e5c-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="94e5c-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94e5c-105">SYNTAX</span></span>

### <span data-ttu-id="94e5c-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="94e5c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e5c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e5c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94e5c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e5c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94e5c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="94e5c-109">DESCRIPTION</span></span>
<span data-ttu-id="94e5c-110">Aktualizuje tabelę Cassandrydy z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94e5c-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="94e5c-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="94e5c-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="94e5c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94e5c-112">EXAMPLES</span></span>

### <span data-ttu-id="94e5c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94e5c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="94e5c-114">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="94e5c-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="94e5c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94e5c-115">PARAMETERS</span></span>

### <span data-ttu-id="94e5c-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94e5c-116">-AccountName</span></span>
<span data-ttu-id="94e5c-117">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="94e5c-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="94e5c-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="94e5c-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="94e5c-119">TTL (Czas wygaśnięcia magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="94e5c-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="94e5c-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="94e5c-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="94e5c-121">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="94e5c-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="94e5c-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94e5c-122">-Confirm</span></span>
<span data-ttu-id="94e5c-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94e5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e5c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e5c-124">-DefaultProfile</span></span>
<span data-ttu-id="94e5c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94e5c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e5c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e5c-126">-InputObject</span></span>
<span data-ttu-id="94e5c-127">Obiekt Cassandra Table.</span><span class="sxs-lookup"><span data-stu-id="94e5c-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="94e5c-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="94e5c-128">-KeyspaceName</span></span>
<span data-ttu-id="94e5c-129">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="94e5c-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="94e5c-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94e5c-130">-Name</span></span>
<span data-ttu-id="94e5c-131">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="94e5c-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="94e5c-132">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="94e5c-132">-ParentObject</span></span>
<span data-ttu-id="94e5c-133">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="94e5c-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="94e5c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e5c-134">-ResourceGroupName</span></span>
<span data-ttu-id="94e5c-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94e5c-135">Name of resource group.</span></span>

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

### <span data-ttu-id="94e5c-136">— Schemat</span><span class="sxs-lookup"><span data-stu-id="94e5c-136">-Schema</span></span>
<span data-ttu-id="94e5c-137">Obiekt PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="94e5c-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="94e5c-138">Użyj New-AzCosmosDBCassandraSchema, aby utworzyć ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="94e5c-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94e5c-139">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="94e5c-139">-Throughput</span></span>
<span data-ttu-id="94e5c-140">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="94e5c-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="94e5c-141">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="94e5c-141">Default value is 400.</span></span>

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

### <span data-ttu-id="94e5c-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="94e5c-142">-TtlInSeconds</span></span>
<span data-ttu-id="94e5c-143">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="94e5c-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="94e5c-144">Jeśli brakuje wartości lub ustawiono wartość - 1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="94e5c-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="94e5c-145">Jeśli wartość jest ustawiona na n, elementy wygasną n sekund po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="94e5c-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="94e5c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e5c-146">-WhatIf</span></span>
<span data-ttu-id="94e5c-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94e5c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e5c-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94e5c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e5c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e5c-149">CommonParameters</span></span>
<span data-ttu-id="94e5c-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e5c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e5c-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94e5c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e5c-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94e5c-152">INPUTS</span></span>

### <span data-ttu-id="94e5c-153">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="94e5c-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="94e5c-154">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="94e5c-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="94e5c-155">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="94e5c-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="94e5c-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94e5c-156">OUTPUTS</span></span>

### <span data-ttu-id="94e5c-157">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="94e5c-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="94e5c-158">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="94e5c-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="94e5c-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94e5c-159">NOTES</span></span>

## <span data-ttu-id="94e5c-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94e5c-160">RELATED LINKS</span></span>
