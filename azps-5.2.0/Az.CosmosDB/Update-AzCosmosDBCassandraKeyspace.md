---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344674"
---
# <span data-ttu-id="e0e89-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="e0e89-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="e0e89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0e89-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e89-103">Umożliwia zaktualizowanie miejsca na CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e0e89-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="e0e89-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą przestrzeń.</span><span class="sxs-lookup"><span data-stu-id="e0e89-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="e0e89-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0e89-105">SYNTAX</span></span>

### <span data-ttu-id="e0e89-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0e89-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e89-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e89-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e89-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e89-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e89-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e0e89-109">DESCRIPTION</span></span>
<span data-ttu-id="e0e89-110">Umożliwia zaktualizowanie miejsca na CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e0e89-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="e0e89-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą przestrzeń.</span><span class="sxs-lookup"><span data-stu-id="e0e89-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="e0e89-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0e89-112">EXAMPLES</span></span>

### <span data-ttu-id="e0e89-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0e89-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="e0e89-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0e89-114">PARAMETERS</span></span>

### <span data-ttu-id="e0e89-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0e89-115">-AccountName</span></span>
<span data-ttu-id="e0e89-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e0e89-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0e89-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e0e89-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e0e89-118">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e0e89-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e0e89-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0e89-119">-Confirm</span></span>
<span data-ttu-id="e0e89-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e89-121">-DefaultProfile</span></span>
<span data-ttu-id="e0e89-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e89-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0e89-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0e89-123">-InputObject</span></span>
<span data-ttu-id="e0e89-124">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="e0e89-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e0e89-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0e89-125">-Name</span></span>
<span data-ttu-id="e0e89-126">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="e0e89-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e0e89-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e0e89-127">-ParentObject</span></span>
<span data-ttu-id="e0e89-128">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e0e89-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e0e89-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e89-129">-ResourceGroupName</span></span>
<span data-ttu-id="e0e89-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0e89-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e0e89-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="e0e89-131">-Throughput</span></span>
<span data-ttu-id="e0e89-132">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e0e89-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e0e89-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="e0e89-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e0e89-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e89-134">-WhatIf</span></span>
<span data-ttu-id="e0e89-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e89-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e89-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0e89-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e89-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e89-137">CommonParameters</span></span>
<span data-ttu-id="e0e89-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e89-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e89-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0e89-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e89-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e89-140">INPUTS</span></span>

### <span data-ttu-id="e0e89-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e0e89-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="e0e89-142">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e0e89-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e0e89-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0e89-143">OUTPUTS</span></span>

### <span data-ttu-id="e0e89-144">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e0e89-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="e0e89-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e0e89-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e0e89-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0e89-146">NOTES</span></span>

## <span data-ttu-id="e0e89-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0e89-147">RELATED LINKS</span></span>
