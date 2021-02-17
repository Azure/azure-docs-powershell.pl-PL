---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196858"
---
# <span data-ttu-id="74caf-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="74caf-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="74caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74caf-102">SYNOPSIS</span></span>
<span data-ttu-id="74caf-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="74caf-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="74caf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74caf-104">SYNTAX</span></span>

### <span data-ttu-id="74caf-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="74caf-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74caf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74caf-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74caf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74caf-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74caf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="74caf-108">DESCRIPTION</span></span>
<span data-ttu-id="74caf-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="74caf-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="74caf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74caf-110">EXAMPLES</span></span>

### <span data-ttu-id="74caf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74caf-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="74caf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74caf-112">PARAMETERS</span></span>

### <span data-ttu-id="74caf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74caf-113">-AccountName</span></span>
<span data-ttu-id="74caf-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="74caf-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74caf-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74caf-115">-Confirm</span></span>
<span data-ttu-id="74caf-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74caf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74caf-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74caf-117">-DatabaseName</span></span>
<span data-ttu-id="74caf-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="74caf-118">Database name.</span></span>

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

### <span data-ttu-id="74caf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74caf-119">-DefaultProfile</span></span>
<span data-ttu-id="74caf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74caf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74caf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74caf-121">-InputObject</span></span>
<span data-ttu-id="74caf-122">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="74caf-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="74caf-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74caf-123">-Name</span></span>
<span data-ttu-id="74caf-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="74caf-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="74caf-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="74caf-125">-ParentObject</span></span>
<span data-ttu-id="74caf-126">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="74caf-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="74caf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74caf-127">-ResourceGroupName</span></span>
<span data-ttu-id="74caf-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74caf-128">Name of resource group.</span></span>

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

### <span data-ttu-id="74caf-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="74caf-129">-ThroughputType</span></span>
<span data-ttu-id="74caf-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="74caf-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="74caf-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="74caf-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="74caf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74caf-132">-WhatIf</span></span>
<span data-ttu-id="74caf-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74caf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74caf-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74caf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74caf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74caf-135">CommonParameters</span></span>
<span data-ttu-id="74caf-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74caf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74caf-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74caf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74caf-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74caf-138">INPUTS</span></span>

### <span data-ttu-id="74caf-139">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="74caf-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="74caf-140">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="74caf-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="74caf-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74caf-141">OUTPUTS</span></span>

### <span data-ttu-id="74caf-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="74caf-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="74caf-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74caf-143">NOTES</span></span>

## <span data-ttu-id="74caf-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74caf-144">RELATED LINKS</span></span>
