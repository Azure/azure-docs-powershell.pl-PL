---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306786"
---
# <span data-ttu-id="6cced-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="6cced-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="6cced-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cced-102">SYNOPSIS</span></span>
<span data-ttu-id="6cced-103">Umożliwia zaktualizowanie kolekcji MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6cced-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="6cced-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="6cced-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="6cced-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cced-105">SYNTAX</span></span>

### <span data-ttu-id="6cced-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6cced-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cced-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cced-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cced-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cced-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cced-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6cced-109">DESCRIPTION</span></span>
<span data-ttu-id="6cced-110">Umożliwia zaktualizowanie kolekcji MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6cced-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="6cced-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="6cced-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="6cced-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cced-112">EXAMPLES</span></span>

### <span data-ttu-id="6cced-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cced-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="6cced-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cced-114">PARAMETERS</span></span>

### <span data-ttu-id="6cced-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6cced-115">-AccountName</span></span>
<span data-ttu-id="6cced-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6cced-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6cced-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="6cced-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="6cced-118">Czas wygaśnięcia (TTL) dla magazynu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="6cced-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="6cced-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6cced-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6cced-120">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="6cced-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6cced-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cced-121">-Confirm</span></span>
<span data-ttu-id="6cced-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cced-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cced-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cced-123">-DatabaseName</span></span>
<span data-ttu-id="6cced-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6cced-124">Database name.</span></span>

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

### <span data-ttu-id="6cced-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cced-125">-DefaultProfile</span></span>
<span data-ttu-id="6cced-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cced-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cced-127">-Index</span><span class="sxs-lookup"><span data-stu-id="6cced-127">-Index</span></span>
<span data-ttu-id="6cced-128">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="6cced-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cced-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6cced-129">-InputObject</span></span>
<span data-ttu-id="6cced-130">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="6cced-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cced-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cced-131">-Name</span></span>
<span data-ttu-id="6cced-132">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="6cced-132">Collection name.</span></span>

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

### <span data-ttu-id="6cced-133">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6cced-133">-ParentObject</span></span>
<span data-ttu-id="6cced-134">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="6cced-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cced-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cced-135">-ResourceGroupName</span></span>
<span data-ttu-id="6cced-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6cced-136">Name of resource group.</span></span>

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

### <span data-ttu-id="6cced-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="6cced-137">-Shard</span></span>
<span data-ttu-id="6cced-138">Ścieżka klucza sharding.</span><span class="sxs-lookup"><span data-stu-id="6cced-138">Sharding key path.</span></span>

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

### <span data-ttu-id="6cced-139">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="6cced-139">-Throughput</span></span>
<span data-ttu-id="6cced-140">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6cced-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="6cced-141">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="6cced-141">Default value is 400.</span></span>

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

### <span data-ttu-id="6cced-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cced-142">-WhatIf</span></span>
<span data-ttu-id="6cced-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cced-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cced-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6cced-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cced-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cced-145">CommonParameters</span></span>
<span data-ttu-id="6cced-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cced-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cced-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cced-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cced-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cced-148">INPUTS</span></span>

### <span data-ttu-id="6cced-149">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6cced-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="6cced-150">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6cced-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="6cced-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cced-151">OUTPUTS</span></span>

### <span data-ttu-id="6cced-152">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6cced-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="6cced-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="6cced-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="6cced-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cced-154">NOTES</span></span>

## <span data-ttu-id="6cced-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cced-155">RELATED LINKS</span></span>
