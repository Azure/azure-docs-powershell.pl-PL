---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977306"
---
# <span data-ttu-id="21eca-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="21eca-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="21eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21eca-102">SYNOPSIS</span></span>
<span data-ttu-id="21eca-103">Aktualizuje kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="21eca-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="21eca-104">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="21eca-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="21eca-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21eca-105">SYNTAX</span></span>

### <span data-ttu-id="21eca-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="21eca-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21eca-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21eca-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21eca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21eca-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21eca-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="21eca-109">DESCRIPTION</span></span>
<span data-ttu-id="21eca-110">Aktualizuje kolekcję ZakonuDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="21eca-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="21eca-111">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą kolekcję.</span><span class="sxs-lookup"><span data-stu-id="21eca-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="21eca-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21eca-112">EXAMPLES</span></span>

### <span data-ttu-id="21eca-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21eca-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="21eca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21eca-114">PARAMETERS</span></span>

### <span data-ttu-id="21eca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21eca-115">-AccountName</span></span>
<span data-ttu-id="21eca-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="21eca-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21eca-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="21eca-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="21eca-118">TTL for Analytical Storage (Czas wygaśnięcia dla magazynu analitycznego).</span><span class="sxs-lookup"><span data-stu-id="21eca-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="21eca-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="21eca-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="21eca-120">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="21eca-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="21eca-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21eca-121">-Confirm</span></span>
<span data-ttu-id="21eca-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21eca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21eca-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21eca-123">-DatabaseName</span></span>
<span data-ttu-id="21eca-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="21eca-124">Database name.</span></span>

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

### <span data-ttu-id="21eca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21eca-125">-DefaultProfile</span></span>
<span data-ttu-id="21eca-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21eca-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21eca-127">-Index</span><span class="sxs-lookup"><span data-stu-id="21eca-127">-Index</span></span>
<span data-ttu-id="21eca-128">Tablica obiektów PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="21eca-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="21eca-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21eca-129">-InputObject</span></span>
<span data-ttu-id="21eca-130">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="21eca-130">Sql Container object.</span></span>

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

### <span data-ttu-id="21eca-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21eca-131">-Name</span></span>
<span data-ttu-id="21eca-132">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="21eca-132">Collection name.</span></span>

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

### <span data-ttu-id="21eca-133">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="21eca-133">-ParentObject</span></span>
<span data-ttu-id="21eca-134">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="21eca-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="21eca-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21eca-135">-ResourceGroupName</span></span>
<span data-ttu-id="21eca-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21eca-136">Name of resource group.</span></span>

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

### <span data-ttu-id="21eca-137">-S s</span><span class="sxs-lookup"><span data-stu-id="21eca-137">-Shard</span></span>
<span data-ttu-id="21eca-138">Ścieżka klucza singa.</span><span class="sxs-lookup"><span data-stu-id="21eca-138">Sharding key path.</span></span>

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

### <span data-ttu-id="21eca-139">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="21eca-139">-Throughput</span></span>
<span data-ttu-id="21eca-140">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="21eca-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="21eca-141">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="21eca-141">Default value is 400.</span></span>

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

### <span data-ttu-id="21eca-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21eca-142">-WhatIf</span></span>
<span data-ttu-id="21eca-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21eca-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21eca-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="21eca-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21eca-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21eca-145">CommonParameters</span></span>
<span data-ttu-id="21eca-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21eca-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21eca-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21eca-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21eca-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21eca-148">INPUTS</span></span>

### <span data-ttu-id="21eca-149">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="21eca-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="21eca-150">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="21eca-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="21eca-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21eca-151">OUTPUTS</span></span>

### <span data-ttu-id="21eca-152">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="21eca-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="21eca-153">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="21eca-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="21eca-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21eca-154">NOTES</span></span>

## <span data-ttu-id="21eca-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21eca-155">RELATED LINKS</span></span>
