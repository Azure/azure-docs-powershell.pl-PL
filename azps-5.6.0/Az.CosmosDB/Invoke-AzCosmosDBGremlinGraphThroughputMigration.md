---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990340"
---
# <span data-ttu-id="3511d-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3511d-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="3511d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3511d-102">SYNOPSIS</span></span>
<span data-ttu-id="3511d-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="3511d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3511d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3511d-104">SYNTAX</span></span>

### <span data-ttu-id="3511d-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3511d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3511d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3511d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3511d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3511d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3511d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3511d-108">DESCRIPTION</span></span>
<span data-ttu-id="3511d-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="3511d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3511d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3511d-110">EXAMPLES</span></span>

### <span data-ttu-id="3511d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3511d-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="3511d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3511d-112">PARAMETERS</span></span>

### <span data-ttu-id="3511d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3511d-113">-AccountName</span></span>
<span data-ttu-id="3511d-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="3511d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3511d-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3511d-115">-Confirm</span></span>
<span data-ttu-id="3511d-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3511d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3511d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3511d-117">-DatabaseName</span></span>
<span data-ttu-id="3511d-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3511d-118">Database name.</span></span>

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

### <span data-ttu-id="3511d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3511d-119">-DefaultProfile</span></span>
<span data-ttu-id="3511d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3511d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3511d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3511d-121">-InputObject</span></span>
<span data-ttu-id="3511d-122">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="3511d-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3511d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3511d-123">-Name</span></span>
<span data-ttu-id="3511d-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="3511d-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="3511d-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3511d-125">-ParentObject</span></span>
<span data-ttu-id="3511d-126">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="3511d-126">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3511d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3511d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3511d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3511d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="3511d-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="3511d-129">-ThroughputType</span></span>
<span data-ttu-id="3511d-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="3511d-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="3511d-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="3511d-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3511d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3511d-132">-WhatIf</span></span>
<span data-ttu-id="3511d-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3511d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3511d-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3511d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3511d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3511d-135">CommonParameters</span></span>
<span data-ttu-id="3511d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3511d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3511d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3511d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3511d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3511d-138">INPUTS</span></span>

### <span data-ttu-id="3511d-139">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3511d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="3511d-140">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="3511d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="3511d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3511d-141">OUTPUTS</span></span>

### <span data-ttu-id="3511d-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3511d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3511d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3511d-143">NOTES</span></span>

## <span data-ttu-id="3511d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3511d-144">RELATED LINKS</span></span>
