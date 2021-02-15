---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196754"
---
# <span data-ttu-id="67d78-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="67d78-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="67d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d78-102">SYNOPSIS</span></span>
<span data-ttu-id="67d78-103">Aktualizuje kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="67d78-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="67d78-104">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="67d78-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="67d78-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67d78-105">SYNTAX</span></span>

### <span data-ttu-id="67d78-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="67d78-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67d78-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67d78-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67d78-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67d78-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67d78-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="67d78-109">DESCRIPTION</span></span>
<span data-ttu-id="67d78-110">Aktualizuje kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="67d78-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="67d78-111">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="67d78-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="67d78-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67d78-112">EXAMPLES</span></span>

### <span data-ttu-id="67d78-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67d78-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="67d78-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d78-114">PARAMETERS</span></span>

### <span data-ttu-id="67d78-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67d78-115">-AccountName</span></span>
<span data-ttu-id="67d78-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="67d78-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="67d78-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="67d78-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="67d78-118">TTL for Analytical Storage (Czas wygaśnięcia dla magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="67d78-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="67d78-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="67d78-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="67d78-120">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="67d78-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="67d78-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67d78-121">-Confirm</span></span>
<span data-ttu-id="67d78-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67d78-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d78-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67d78-123">-DatabaseName</span></span>
<span data-ttu-id="67d78-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="67d78-124">Database name.</span></span>

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

### <span data-ttu-id="67d78-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d78-125">-DefaultProfile</span></span>
<span data-ttu-id="67d78-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67d78-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d78-127">-Index</span><span class="sxs-lookup"><span data-stu-id="67d78-127">-Index</span></span>
<span data-ttu-id="67d78-128">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="67d78-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="67d78-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67d78-129">-InputObject</span></span>
<span data-ttu-id="67d78-130">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="67d78-130">Sql Container object.</span></span>

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

### <span data-ttu-id="67d78-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67d78-131">-Name</span></span>
<span data-ttu-id="67d78-132">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="67d78-132">Collection name.</span></span>

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

### <span data-ttu-id="67d78-133">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="67d78-133">-ParentObject</span></span>
<span data-ttu-id="67d78-134">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="67d78-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="67d78-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d78-135">-ResourceGroupName</span></span>
<span data-ttu-id="67d78-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67d78-136">Name of resource group.</span></span>

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

### <span data-ttu-id="67d78-137">-S s</span><span class="sxs-lookup"><span data-stu-id="67d78-137">-Shard</span></span>
<span data-ttu-id="67d78-138">Ścieżka klucza singa.</span><span class="sxs-lookup"><span data-stu-id="67d78-138">Sharding key path.</span></span>

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

### <span data-ttu-id="67d78-139">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="67d78-139">-Throughput</span></span>
<span data-ttu-id="67d78-140">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="67d78-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="67d78-141">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="67d78-141">Default value is 400.</span></span>

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

### <span data-ttu-id="67d78-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d78-142">-WhatIf</span></span>
<span data-ttu-id="67d78-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d78-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d78-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67d78-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d78-145">CommonParameters</span></span>
<span data-ttu-id="67d78-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d78-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d78-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d78-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67d78-148">INPUTS</span></span>

### <span data-ttu-id="67d78-149">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="67d78-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="67d78-150">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="67d78-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="67d78-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67d78-151">OUTPUTS</span></span>

### <span data-ttu-id="67d78-152">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="67d78-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="67d78-153">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="67d78-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="67d78-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67d78-154">NOTES</span></span>

## <span data-ttu-id="67d78-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67d78-155">RELATED LINKS</span></span>
