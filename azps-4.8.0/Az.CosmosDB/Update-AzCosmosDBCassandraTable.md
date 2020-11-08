---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223574"
---
# <span data-ttu-id="4ac0a-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4ac0a-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4ac0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ac0a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac0a-103">Umożliwia zaktualizowanie tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="4ac0a-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="4ac0a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ac0a-105">SYNTAX</span></span>

### <span data-ttu-id="4ac0a-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4ac0a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac0a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac0a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ac0a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac0a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ac0a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4ac0a-109">DESCRIPTION</span></span>
<span data-ttu-id="4ac0a-110">Umożliwia zaktualizowanie tabeli Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="4ac0a-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą tabelę.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="4ac0a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ac0a-112">EXAMPLES</span></span>

### <span data-ttu-id="4ac0a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ac0a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="4ac0a-114">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="4ac0a-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="4ac0a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ac0a-115">PARAMETERS</span></span>

### <span data-ttu-id="4ac0a-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ac0a-116">-AccountName</span></span>
<span data-ttu-id="4ac0a-117">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4ac0a-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="4ac0a-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="4ac0a-119">Czas wygaśnięcia magazynu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="4ac0a-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4ac0a-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4ac0a-121">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4ac0a-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ac0a-122">-Confirm</span></span>
<span data-ttu-id="4ac0a-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac0a-124">-DefaultProfile</span></span>
<span data-ttu-id="4ac0a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac0a-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ac0a-126">-InputObject</span></span>
<span data-ttu-id="4ac0a-127">Obiekt tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="4ac0a-128">-Spacename</span><span class="sxs-lookup"><span data-stu-id="4ac0a-128">-KeyspaceName</span></span>
<span data-ttu-id="4ac0a-129">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4ac0a-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ac0a-130">-Name</span></span>
<span data-ttu-id="4ac0a-131">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4ac0a-132">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="4ac0a-132">-ParentObject</span></span>
<span data-ttu-id="4ac0a-133">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4ac0a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac0a-134">-ResourceGroupName</span></span>
<span data-ttu-id="4ac0a-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-135">Name of resource group.</span></span>

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

### <span data-ttu-id="4ac0a-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="4ac0a-136">-Schema</span></span>
<span data-ttu-id="4ac0a-137">Obiekt PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="4ac0a-138">Użyj New-AzCosmosDBCassandraSchema, aby utworzyć ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="4ac0a-139">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="4ac0a-139">-Throughput</span></span>
<span data-ttu-id="4ac0a-140">Przepływność przestrzeni Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4ac0a-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="4ac0a-141">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-141">Default value is 400.</span></span>

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

### <span data-ttu-id="4ac0a-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="4ac0a-142">-TtlInSeconds</span></span>
<span data-ttu-id="4ac0a-143">Domyślny czas wygaśnięcia (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="4ac0a-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="4ac0a-144">Jeśli wartość jest brakująca lub ustawiona na wartość-1, elementy nie wygasają.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="4ac0a-145">Jeśli wartość jest ustawiona na n, elementy wygasną po n sekundach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="4ac0a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac0a-146">-WhatIf</span></span>
<span data-ttu-id="4ac0a-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac0a-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac0a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac0a-149">CommonParameters</span></span>
<span data-ttu-id="4ac0a-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac0a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac0a-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ac0a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac0a-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ac0a-152">INPUTS</span></span>

### <span data-ttu-id="4ac0a-153">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="4ac0a-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="4ac0a-154">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4ac0a-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="4ac0a-155">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4ac0a-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="4ac0a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ac0a-156">OUTPUTS</span></span>

### <span data-ttu-id="4ac0a-157">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4ac0a-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="4ac0a-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="4ac0a-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="4ac0a-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ac0a-159">NOTES</span></span>

## <span data-ttu-id="4ac0a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ac0a-160">RELATED LINKS</span></span>
