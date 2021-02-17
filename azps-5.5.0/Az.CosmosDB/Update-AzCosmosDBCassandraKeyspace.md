---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177219"
---
# <span data-ttu-id="c0864-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="c0864-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="c0864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0864-102">SYNOPSIS</span></span>
<span data-ttu-id="c0864-103">Aktualizuje spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="c0864-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c0864-104">Wykonuje operację poprawiania po stronie klienta, czytając istniejącą klawisz Keyspace.</span><span class="sxs-lookup"><span data-stu-id="c0864-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c0864-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0864-105">SYNTAX</span></span>

### <span data-ttu-id="c0864-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0864-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0864-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0864-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0864-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0864-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0864-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0864-109">DESCRIPTION</span></span>
<span data-ttu-id="c0864-110">Aktualizuje spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="c0864-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c0864-111">Wykonuje operację poprawiania po stronie klienta, czytając istniejącą klawisz Keyspace.</span><span class="sxs-lookup"><span data-stu-id="c0864-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c0864-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0864-112">EXAMPLES</span></span>

### <span data-ttu-id="c0864-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0864-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="c0864-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0864-114">PARAMETERS</span></span>

### <span data-ttu-id="c0864-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0864-115">-AccountName</span></span>
<span data-ttu-id="c0864-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c0864-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0864-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c0864-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c0864-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="c0864-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c0864-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0864-119">-Confirm</span></span>
<span data-ttu-id="c0864-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0864-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0864-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0864-121">-DefaultProfile</span></span>
<span data-ttu-id="c0864-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0864-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0864-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0864-123">-InputObject</span></span>
<span data-ttu-id="c0864-124">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="c0864-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c0864-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0864-125">-Name</span></span>
<span data-ttu-id="c0864-126">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c0864-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c0864-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0864-127">-ParentObject</span></span>
<span data-ttu-id="c0864-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="c0864-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c0864-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0864-129">-ResourceGroupName</span></span>
<span data-ttu-id="c0864-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0864-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c0864-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="c0864-131">-Throughput</span></span>
<span data-ttu-id="c0864-132">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c0864-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c0864-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="c0864-133">Default value is 400.</span></span>

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

### <span data-ttu-id="c0864-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0864-134">-WhatIf</span></span>
<span data-ttu-id="c0864-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0864-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0864-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0864-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0864-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0864-137">CommonParameters</span></span>
<span data-ttu-id="c0864-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0864-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0864-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0864-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0864-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0864-140">INPUTS</span></span>

### <span data-ttu-id="c0864-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c0864-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="c0864-142">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c0864-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c0864-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0864-143">OUTPUTS</span></span>

### <span data-ttu-id="c0864-144">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c0864-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c0864-145">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c0864-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c0864-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0864-146">NOTES</span></span>

## <span data-ttu-id="c0864-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0864-147">RELATED LINKS</span></span>
