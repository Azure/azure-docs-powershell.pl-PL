---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181322"
---
# <span data-ttu-id="3576a-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="3576a-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="3576a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3576a-102">SYNOPSIS</span></span>
<span data-ttu-id="3576a-103">Tworzy nową spację Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="3576a-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="3576a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3576a-104">SYNTAX</span></span>

### <span data-ttu-id="3576a-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3576a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3576a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3576a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3576a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3576a-107">DESCRIPTION</span></span>
<span data-ttu-id="3576a-108">Tworzy nową spację Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="3576a-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="3576a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3576a-109">EXAMPLES</span></span>

### <span data-ttu-id="3576a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3576a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="3576a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3576a-111">PARAMETERS</span></span>

### <span data-ttu-id="3576a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3576a-112">-AccountName</span></span>
<span data-ttu-id="3576a-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="3576a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3576a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3576a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3576a-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="3576a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3576a-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3576a-116">-Confirm</span></span>
<span data-ttu-id="3576a-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3576a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3576a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3576a-118">-DefaultProfile</span></span>
<span data-ttu-id="3576a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3576a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3576a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3576a-120">-Name</span></span>
<span data-ttu-id="3576a-121">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3576a-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="3576a-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3576a-122">-ParentObject</span></span>
<span data-ttu-id="3576a-123">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="3576a-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3576a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3576a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3576a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3576a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3576a-126">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="3576a-126">-Throughput</span></span>
<span data-ttu-id="3576a-127">Przepływność klawiszy Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="3576a-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="3576a-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="3576a-128">Default value is 400.</span></span>

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

### <span data-ttu-id="3576a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3576a-129">-WhatIf</span></span>
<span data-ttu-id="3576a-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3576a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3576a-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3576a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3576a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3576a-132">CommonParameters</span></span>
<span data-ttu-id="3576a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3576a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3576a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3576a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3576a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3576a-135">INPUTS</span></span>

### <span data-ttu-id="3576a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3576a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3576a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3576a-137">OUTPUTS</span></span>

### <span data-ttu-id="3576a-138">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="3576a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="3576a-139">Microsoft.Azure.Commands.Dosdb.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="3576a-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3576a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3576a-140">NOTES</span></span>

## <span data-ttu-id="3576a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3576a-141">RELATED LINKS</span></span>
