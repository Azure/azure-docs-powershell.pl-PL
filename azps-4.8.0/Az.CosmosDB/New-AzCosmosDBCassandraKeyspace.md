---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064223"
---
# <span data-ttu-id="0c6e6-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="0c6e6-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="0c6e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6e6-103">Tworzy nowy CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0c6e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c6e6-104">SYNTAX</span></span>

### <span data-ttu-id="0c6e6-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c6e6-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6e6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6e6-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c6e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c6e6-107">DESCRIPTION</span></span>
<span data-ttu-id="0c6e6-108">Tworzy nowy CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0c6e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c6e6-109">EXAMPLES</span></span>

### <span data-ttu-id="0c6e6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c6e6-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="0c6e6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c6e6-111">PARAMETERS</span></span>

### <span data-ttu-id="0c6e6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c6e6-112">-AccountName</span></span>
<span data-ttu-id="0c6e6-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c6e6-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0c6e6-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0c6e6-115">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0c6e6-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c6e6-116">-Confirm</span></span>
<span data-ttu-id="0c6e6-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6e6-118">-DefaultProfile</span></span>
<span data-ttu-id="0c6e6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6e6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c6e6-120">-Name</span></span>
<span data-ttu-id="0c6e6-121">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0c6e6-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0c6e6-122">-ParentObject</span></span>
<span data-ttu-id="0c6e6-123">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0c6e6-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0c6e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c6e6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0c6e6-126">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="0c6e6-126">-Throughput</span></span>
<span data-ttu-id="0c6e6-127">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0c6e6-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="0c6e6-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-128">Default value is 400.</span></span>

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

### <span data-ttu-id="0c6e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6e6-129">-WhatIf</span></span>
<span data-ttu-id="0c6e6-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6e6-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6e6-132">CommonParameters</span></span>
<span data-ttu-id="0c6e6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6e6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c6e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6e6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c6e6-135">INPUTS</span></span>

### <span data-ttu-id="0c6e6-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0c6e6-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0c6e6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c6e6-137">OUTPUTS</span></span>

### <span data-ttu-id="0c6e6-138">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0c6e6-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="0c6e6-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0c6e6-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0c6e6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c6e6-140">NOTES</span></span>

## <span data-ttu-id="0c6e6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c6e6-141">RELATED LINKS</span></span>
