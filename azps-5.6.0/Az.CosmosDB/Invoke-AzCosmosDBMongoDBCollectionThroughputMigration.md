---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 230fb5f43bceda32489ac632cb995eb5e4adac25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972074"
---
# <span data-ttu-id="dbf2f-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="dbf2f-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="dbf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf2f-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="dbf2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbf2f-104">SYNTAX</span></span>

### <span data-ttu-id="dbf2f-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dbf2f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf2f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf2f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf2f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf2f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbf2f-108">DESCRIPTION</span></span>
<span data-ttu-id="dbf2f-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="dbf2f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbf2f-110">EXAMPLES</span></span>

### <span data-ttu-id="dbf2f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dbf2f-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="dbf2f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbf2f-112">PARAMETERS</span></span>

### <span data-ttu-id="dbf2f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbf2f-113">-AccountName</span></span>
<span data-ttu-id="dbf2f-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dbf2f-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbf2f-115">-Confirm</span></span>
<span data-ttu-id="dbf2f-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf2f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbf2f-117">-DatabaseName</span></span>
<span data-ttu-id="dbf2f-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-118">Database name.</span></span>

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

### <span data-ttu-id="dbf2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf2f-119">-DefaultProfile</span></span>
<span data-ttu-id="dbf2f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf2f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf2f-121">-InputObject</span></span>
<span data-ttu-id="dbf2f-122">Obiekt Mongo Collection.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="dbf2f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dbf2f-123">-Name</span></span>
<span data-ttu-id="dbf2f-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-124">Collection name.</span></span>

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

### <span data-ttu-id="dbf2f-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbf2f-125">-ParentObject</span></span>
<span data-ttu-id="dbf2f-126">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="dbf2f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf2f-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbf2f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dbf2f-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="dbf2f-129">-ThroughputType</span></span>
<span data-ttu-id="dbf2f-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="dbf2f-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="dbf2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf2f-132">-WhatIf</span></span>
<span data-ttu-id="dbf2f-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf2f-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf2f-135">CommonParameters</span></span>
<span data-ttu-id="dbf2f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf2f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbf2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf2f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbf2f-138">INPUTS</span></span>

### <span data-ttu-id="dbf2f-139">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="dbf2f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="dbf2f-140">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="dbf2f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="dbf2f-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbf2f-141">OUTPUTS</span></span>

### <span data-ttu-id="dbf2f-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dbf2f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dbf2f-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbf2f-143">NOTES</span></span>

## <span data-ttu-id="dbf2f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbf2f-144">RELATED LINKS</span></span>
