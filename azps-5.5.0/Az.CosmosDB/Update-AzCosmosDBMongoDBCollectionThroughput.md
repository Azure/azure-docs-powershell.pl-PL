---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196747"
---
# <span data-ttu-id="05889-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="05889-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="05889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05889-102">SYNOPSIS</span></span>
<span data-ttu-id="05889-103">Aktualizuje wartość przepływności kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="05889-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="05889-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05889-104">SYNTAX</span></span>

### <span data-ttu-id="05889-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="05889-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05889-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05889-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05889-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05889-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05889-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="05889-108">DESCRIPTION</span></span>
<span data-ttu-id="05889-109">Aktualizuje wartość przepływności kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="05889-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="05889-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05889-110">EXAMPLES</span></span>

### <span data-ttu-id="05889-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05889-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="05889-112">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="05889-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="05889-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05889-113">PARAMETERS</span></span>

### <span data-ttu-id="05889-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="05889-114">-AccountName</span></span>
<span data-ttu-id="05889-115">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="05889-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="05889-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="05889-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="05889-117">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="05889-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="05889-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05889-118">-Confirm</span></span>
<span data-ttu-id="05889-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05889-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05889-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05889-120">-DatabaseName</span></span>
<span data-ttu-id="05889-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="05889-121">Database name.</span></span>

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

### <span data-ttu-id="05889-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05889-122">-DefaultProfile</span></span>
<span data-ttu-id="05889-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="05889-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05889-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05889-124">-InputObject</span></span>
<span data-ttu-id="05889-125">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="05889-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="05889-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="05889-126">-Name</span></span>
<span data-ttu-id="05889-127">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="05889-127">Collection name.</span></span>

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

### <span data-ttu-id="05889-128">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="05889-128">-ParentObject</span></span>
<span data-ttu-id="05889-129">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="05889-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="05889-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05889-130">-ResourceGroupName</span></span>
<span data-ttu-id="05889-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05889-131">Name of resource group.</span></span>

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

### <span data-ttu-id="05889-132">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="05889-132">-Throughput</span></span>
<span data-ttu-id="05889-133">Przepływność kontenerów SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="05889-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="05889-134">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="05889-134">Default value is 400.</span></span>

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

### <span data-ttu-id="05889-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05889-135">-WhatIf</span></span>
<span data-ttu-id="05889-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05889-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05889-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05889-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05889-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05889-138">CommonParameters</span></span>
<span data-ttu-id="05889-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05889-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05889-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05889-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05889-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05889-141">INPUTS</span></span>

### <span data-ttu-id="05889-142">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="05889-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="05889-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05889-143">OUTPUTS</span></span>

### <span data-ttu-id="05889-144">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="05889-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="05889-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05889-145">NOTES</span></span>

## <span data-ttu-id="05889-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05889-146">RELATED LINKS</span></span>
