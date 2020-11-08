---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053405"
---
# <span data-ttu-id="6c1a0-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="6c1a0-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="6c1a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1a0-103">Umożliwia ustawienie tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="6c1a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c1a0-104">SYNTAX</span></span>

### <span data-ttu-id="6c1a0-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c1a0-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c1a0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c1a0-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c1a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c1a0-107">DESCRIPTION</span></span>
<span data-ttu-id="6c1a0-108">Polecenie cmdlet **Set-AzCosmosDBCassandraTable** ustawia CosmosDB Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6c1a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c1a0-109">EXAMPLES</span></span>

### <span data-ttu-id="6c1a0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c1a0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="6c1a0-111">Obiekt zasobu zawiera wartości właściwości _rid, _ts, _etag, DefaultTtl i schematu.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="6c1a0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c1a0-112">PARAMETERS</span></span>

### <span data-ttu-id="6c1a0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c1a0-113">-AccountName</span></span>
<span data-ttu-id="6c1a0-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6c1a0-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c1a0-115">-Confirm</span></span>
<span data-ttu-id="6c1a0-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1a0-117">-DefaultProfile</span></span>
<span data-ttu-id="6c1a0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c1a0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c1a0-119">-InputObject</span></span>
<span data-ttu-id="6c1a0-120">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="6c1a0-121">-Spacename</span><span class="sxs-lookup"><span data-stu-id="6c1a0-121">-KeyspaceName</span></span>
<span data-ttu-id="6c1a0-122">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6c1a0-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c1a0-123">-Name</span></span>
<span data-ttu-id="6c1a0-124">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="6c1a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c1a0-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6c1a0-127">-Schema</span><span class="sxs-lookup"><span data-stu-id="6c1a0-127">-Schema</span></span>
<span data-ttu-id="6c1a0-128">Obiekt PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="6c1a0-129">Użyj New-AzCosmosDBCassandraSchema, aby utworzyć ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="6c1a0-130">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="6c1a0-130">-Throughput</span></span>
<span data-ttu-id="6c1a0-131">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6c1a0-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="6c1a0-132">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-132">Default value is 400.</span></span>

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

### <span data-ttu-id="6c1a0-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6c1a0-133">-TtlInSeconds</span></span>
<span data-ttu-id="6c1a0-134">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="6c1a0-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="6c1a0-135">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="6c1a0-136">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="6c1a0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1a0-137">-WhatIf</span></span>
<span data-ttu-id="6c1a0-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c1a0-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1a0-140">CommonParameters</span></span>
<span data-ttu-id="6c1a0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c1a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1a0-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c1a0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1a0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c1a0-143">INPUTS</span></span>

### <span data-ttu-id="6c1a0-144">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="6c1a0-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="6c1a0-145">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6c1a0-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="6c1a0-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c1a0-146">OUTPUTS</span></span>

### <span data-ttu-id="6c1a0-147">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="6c1a0-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="6c1a0-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c1a0-148">NOTES</span></span>

## <span data-ttu-id="6c1a0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c1a0-149">RELATED LINKS</span></span>
